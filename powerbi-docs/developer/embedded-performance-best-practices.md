---
title: Bästa praxis för Power BI Embedded-prestanda
description: Den här artikeln innehåller riktlinjer för bästa praxis för inbäddad analys
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-embedded
ms.topic: conceptual
ms.date: 12/12/2018
ms.openlocfilehash: d0f4ca29e30e5f6e6176f036dc535601eb580471
ms.sourcegitcommit: 298db44200b78b1281b3ae6dfe7cce7a89865ec9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/13/2018
ms.locfileid: "53329888"
---
# <a name="power-bi-embedded-performance-best-practices"></a>Bästa praxis för Power BI Embedded-prestanda

Den här artikeln innehåller rekommendationer för snabbare återgivning av rapporter, instrumentpaneler och paneler i ditt program

## <a name="embed-parameters"></a>Parametrar för inbäddning

Powerbi.embed()-metoden tar emot ett fåtal parametrar för att bädda in en rapport, en instrumentpanel eller en panel. Dessa parametrar påverkar prestandan.

### <a name="embed-url"></a>Inbäddnings-URL

Undvik att generera inbäddnings-URL:en själv. Se i stället till att hämta inbäddnings-URL:en genom att anropa API:et för att [hämta rapporter](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Frest%2Fapi%2Fpower-bi%2Freports%2Fgetreportsingroup&data=02%7C01%7CMark.Ghanayem%40microsoft.com%7C07ca68ceb37a48e3f3de08d64968707a%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636777110256168308&sdata=22lkqRM2w1MQfrM8dooedaPqqIU8PufTq9TT4VDzRo0%3D&reserved=0), [hämta instrumentpaneler](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Frest%2Fapi%2Fpower-bi%2Fdashboards%2Fgetdashboardsingroup&data=02%7C01%7CMark.Ghanayem%40microsoft.com%7C07ca68ceb37a48e3f3de08d64968707a%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636777110256168308&sdata=nfWRgbSoXVF42Rg%2Ba9491u19uksXp%2FAyz%2Fa%2Ba7%2FCtdA%3D&reserved=0) eller [hämta paneler](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Frest%2Fapi%2Fpower-bi%2Fdashboards%2Fgettilesingroup&data=02%7C01%7CMark.Ghanayem%40microsoft.com%7C07ca68ceb37a48e3f3de08d64968707a%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636777110256178318&sdata=LgZ27TynNpqQJDrb3aHWGQXIS%2FzichAO9De5M2uhF1Q%3D&reserved=0). Vi har lagt till en ny parameter till URL-adressen som heter **_config_** och som används för att förbättra prestandan.

### <a name="permissions"></a>Behörigheter

Ange **visnings**behörigheter om du inte har för avsikt att bädda in en rapport i **redigeringsläget**. På så sätt initierar inbäddningskod inte komponenter som används för redigeringsläge.

### <a name="filters-bookmarks-and-slicers"></a>Filter, bokmärken och utsnitt

Vanligtvis sparas visuella rapportobjekt med cachelagrade data. Cachelagrade data används för att ge upplevd prestanda. Rapporter återger cachelagrade data medan frågor körs. Om filter, bokmärken eller utsnitt tillhandahålls är cachelagrade data inte relevanta. Då återges de visuella objekten först efter att den visuella frågan har körts.

Om du bäddar in rapporter med samma filter måste du spara rapporten med filter som redan tillämpats för att undvika att skicka en lista över filter i konfigurationen som ska läsas in.

## <a name="preload"></a>Förinläsning

Använd JavaScript-API:et *preload* (förinläsning) för att förbättra prestandan för slutanvändaren.
Powerbi.preload() laddar ned javascript, css-filer och andra artefakter som används senare för att bädda in en rapport.

Anropa preload om du inte tänker bädda in rapporten direkt. Om du till exempel bäddar in en rapport med ett knapptryck är det bättre att anropa preload när den föregående sidan laddar. Då är återgivningen snabbare när programanvändaren sedan klickar på knappen.

## <a name="measure-performance"></a>Mäta prestanda

Använd följande om du vill mäta prestandan:

1. Loaded (Inläst): tid tills rapporten har initierats (användaren ser ingen rotationssymbol).
2. Rendered (Återgett): tid tills den fullständiga rapporten återges med faktiska data. Den återgivna händelsen utlöses varje gång rapporten återges på nytt (det vill säga efter att filter tillämpas). När du mäter en rapport bör du först se till att utföra beräkningarna i den händelse som aktiveras först.

Cachelagrade data återges när de är tillgängliga, men vi har inte en händelse för dessa data än.

## <a name="update-tools-and-sdk-packages"></a>Uppdatera verktyg och SDK-paket

Se till att verktyg och SDK-paket är uppdaterade.

* Använd alltid den senaste versionen av [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).

* Installera den senaste versionen av [Power BI-klientens SDK](https://github.com/Microsoft/PowerBI-JavaScript). Vi släpper kontinuerligt fler förbättringar, så se till att kontrollera dem med jämna mellanrum.

* Paket att installera:
    * Npm-paket: powerbi-client
    * NuGet-paket: Microsoft.PowerBI.JavaScript

> [!Note]
> Kom ihåg att inläsningstid främst är beroende av de element som är relevanta för rapporten och själva datan. Till exempel antalet visuella objekt, datastorleken, frågornas komplexitet och beräknade mått. Följ gärna [bästa praxis](../power-bi-reports-performance.md) för att förbättra rapportens inläsningstid.

## <a name="next-steps"></a>Nästa steg

* [Rapportprestanda](../power-bi-reports-performance.md)
* [Så här felsöker du problem i Power BI Embedded](embedded-troubleshoot.md)
* [Vanliga frågor och svar om Power BI Embedded](embedded-faq.md)