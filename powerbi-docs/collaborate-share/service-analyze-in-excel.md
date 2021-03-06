---
title: Analysera i Excel för Power BI
description: Lär dig mer om hur du kan analysera Power BI-datauppsättningar i Excel
author: davidiseminger
ms.reviewer: ''
ms.custom: contperfq4
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/06/2020
ms.author: davidi
LocalizationGroup: Reports
ms.openlocfilehash: 48e1df6f8d47b996145d8734f89b2e15d17abf9c
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/13/2020
ms.locfileid: "83275074"
---
# <a name="analyze-in-excel"></a>Analysera i Excel
Det finns tillfällen när du kanske vill använda Excel för att visa och interagera med en datauppsättning som du har i Power BI. Med **Analysera i Excel** kan du göra just det och komma åt funktionerna för pivottabell, diagram och utsnitt i Excel baserat på den datauppsättning som finns i Power BI.

## <a name="two-ways-to-get-started"></a>Två sätt att komma igång
Det finns två olika sätt att utforska Power BI-datauppsättningar i Excel – om du börjar från Power BI följer du stegen som beskrivs i det här dokumentet.  Det finns också möjlighet för användare med vissa Office-SKU:er att komma åt sina datauppsättningar direkt från funktionen Hämta data i en Excel-arbetsbok.  Användarna kan bläddra bland de datauppsättningar som de har åtkomst till, se om datauppsättningar är certifierade eller upphöjda och om dataskyddsetiketter har tillämpats.  Mer information om den här funktionen finns i [Create a PivotTable from Power BI datasets](https://support.office.com/article/31444a04-9c38-4dd7-9a45-22848c666884) (Skapa en pivottabell från Power BI-datauppsättningar) i Excel-dokumentationen.

## <a name="requirements"></a>Krav
Det finns några krav för att använda **Analysera i Excel**:

* **Analysera i Excel** stöds för Microsoft Excel 2010 SP1 och senare.

* Pivottabeller i Excel stöder inte dra och släpp-aggregering av numeriska fält. Datauppsättningen i Power BI *måste ha fördefinierade mått*. Läs om att [skapa mått](../transform-model/desktop-measures.md).
* Vissa organisationer kan ha grupprincipregler som förhindrar installation av nödvändiga **Analysera i Excel**-uppdateringar i Excel. Kontrollera med administratören om det inte går att installera uppdateringarna.
* **Analysera i Excel** kräver att datauppsättningen finns i Power BI Premium eller att användaren har en Power BI Pro-licens. Mer information om skillnaderna i funktionalitet mellan de olika licenstyperna finns i _Jämförelse av Power BI-funktioner_ i [Power BI-prissättning](https://powerbi.microsoft.com/pricing/).
* Användare kan ansluta till datamängder via Analysera i Excel om de har behörighet till den underliggande datamängden.  En användare kan ha sådan behörighet på flera olika sätt, till exempel genom att vara medlem i arbetsytan som innehåller datamängden, få en rapport eller instrumentpanel delad till sig där datamängden används eller ha skapandebehörighet till datamängden via en arbetsyta eller app som innehåller datamängden. Läs mer om [behörigheten Skapa](../connect-data/service-datasets-build-permissions.md) för datamängder.
* Gästanvändare kan inte använda **Analysera i Excel** för datamängder som skickas från en annan klientorganisation. 
* **Analysera i Excel** är en funktion i Power BI-tjänsten och är inte tillgänglig i Power BI Report Server eller Power BI Embedded. 
* **Analysera i Excel** stöds bara för datorer som kör Microsoft Windows.

## <a name="how-does-it-work"></a>Hur fungerar det?
När du väljer **Analysera i Excel** på menyn **Fler alternativ** (...) som är associerad med en datamängd eller rapport i **Power BI** så skapar Power BI en .ODC-fil och laddar ned den från webbläsaren till din dator.

![Analysera i Excel](media/service-analyze-in-excel/power-bi-analyze-in-excel.png)

När du öppnar filen i Excel, visas en tom **pivottabell** och en **Fält**-lista med tabeller, fält och mått från Power BI-datauppsättningen. Du kan skapa pivottabeller och diagram och analysera din datauppsättning precis som om du arbetade med en lokal datauppsättning i Excel.

Odc-filen har en MSOLAP-anslutningssträng som ansluter till din datauppsättning i Power BI. När du analyserar eller arbetar med dina data, ställer Excel frågor till datauppsättningen i Power BI och returnerar resultaten till Excel. Om datauppsättningen ansluter till en datakälla i realtid med hjälp av DirectQuery, frågar Power BI datakällan och returnerar resultatet till Excel.

**Analysera i Excel** är mycket användbart för datauppsättningar och rapporter som ansluter till *Analysis Services-tabeller* eller *flerdimensionella* databaser, eller från Power BI Desktop-filer eller Excel-arbetsböcker med datamodeller vars modellmått skapas med hjälp av Data Analysis-uttryck (DAX).

## <a name="get-started-with-analyze-in-excel-in-power-bi"></a>Kom igång med Analysera i Excel i Power BI
Välj menyn **Fler alternativ** bredvid en rapport eller datamängd i Power BI (... bredvid namnet på rapporten eller datamängden) och välj **Analysera i Excel** på menyn som visas.

![Analysera i Excel](media/service-analyze-in-excel/power-bi-analyze-menu.png)

### <a name="install-excel-updates"></a>Installera Excel-uppdateringar
När du använder **Analysera i Excel** för första gången, måste du installera uppdateringar av Excel-biblioteken. Du uppmanas att ladda ned och köra Excel-uppdateringar (detta startar installationen av *SQL_AS_OLEDDB.msi*, Windows installationspaket). Det här paketet installerar **Microsoft Analysis Services OLE DB-provider för Microsoft SQL Server 2016 RC0 (förhandsversion)** .

> [!NOTE]
> Var noga med att markera **Visa inte detta igen** i dialogrutan **Installera Excel-uppdateringar**. Du behöver bara installera uppdateringen en gång.
> 
> 

![Kryssrutan Visa inte detta igen](media/service-analyze-in-excel/pbi_anlz_excel_dontshow.png)

Om du behöver installera Excel-uppdateringarna för **Analysera i Excel** igen, kan du hämta dem från **hämtningsikonen** i Power BI, enligt följande bild.

![Installera uppdateringar](media/service-analyze-in-excel/pbi_anlz_excel_download_again.png)

### <a name="sign-in-to-power-bi"></a>Logga in i Power BI
Även om du är inloggad i Power BI i webbläsaren, kan du första gången du öppnar en ny odc-fil i Excel bli ombedd att logga in i Power BI med ditt Power BI-konto. Detta autentiserar anslutningen från Excel till Power BI.

### <a name="users-with-multiple-power-bi-accounts"></a>Användare med flera Power BI-konton
Vissa användare har flera Power BI-konton och dessa användare kan råka ut för en situation där de är inloggade i Power BI med ett konto, men det konto som har åtkomst till den datauppsättning som används i Analysera i Excel är ett annat konto. I dessa fall kan du få ett meddelande om **förbud** eller inloggningsfel när du försöker komma åt en datauppsättning som används i en Analysera i Excel-arbetsbok.

Du ges en ny möjlighet att logga in och då kan du logga in med det Power BI-konto som har åtkomst till datauppsättningen som används av Analysera i Excel. Du kan även välja ditt namn i det övre menyfliksområdet i Excel, som identifierar vilket konto du för närvarande är inloggad med. Logga ut och logga in med ett annat konto.

### <a name="enable-data-connections"></a>Aktivera dataanslutningar
För att analysera dina Power BI-data i Excel, uppmanas du att kontrollera filnamnet och sökvägen för odc-filen och sedan välja **Aktivera**.

![Aktivera dataanslutningar](media/service-analyze-in-excel/pbi_anlz_excel_enable.png)

> [!NOTE]
> Administratörer för Power BI-klienter kan använda *Power BI-administratörsportalen* för att inaktivera användningen av **Analysera i Excel** med lokala datauppsättningar som förvaras i Analysis Services-databaser. När alternativet är inaktiverat, är **Analysera i Excel** inaktiverat för Analysis Services-databaser, men fortsätter att vara tillgängligt för användning med andra datauppsättningar.
> 
> 

## <a name="analyze-away"></a>Analysera mera
Nu när Excel har öppnats och du har en tom pivottabell, är du redo att göra alla typer av analyser med din Power BI-datauppsättning. Precis som för andra lokala arbetsböcker kan du med Analysera i Excel skapa pivottabeller och diagram, lägga till data från andra källor och så vidare. Och naturligtvis kan du skapa olika kalkylblad med alla typer av vyer för dina data.

![Pivottabell och pivotdiagram i Excel](media/service-analyze-in-excel/pbi_anlz_excel_chart.png)

> [!NOTE]
> Det är viktigt att veta att användning av **Analysera i Excel** visar alla data på detaljnivå för alla användare med behörighet för datauppsättningen.
> 
> 

## <a name="save"></a>Spara
Du kan spara den här Power BI-datauppsättningsanslutna arbetsboken precis som vilken arbetsbok som helst. Du kan dock inte publicera eller importera arbetsboken tillbaka till Power BI eftersom du bara kan publicera eller importera arbetsböcker till Power BI som har data i tabeller eller som har en datamodell. Eftersom den nya arbetsboken bara har en anslutning till datauppsättningen i Power BI, skulle det bara vara att gå runt i cirklar att publicera eller importera den till Power BI!

## <a name="share"></a>Dela
När din arbetsbok har sparats kan du dela den med andra Power BI-användare i din organisation.

När en användare som du har delat arbetsboken med öppnar arbetsboken, ser han eller hon dina pivottabeller och data som de visades när arbetsboken senast sparades, vilket inte nödvändigtvis är den senaste versionen av dina data. För att hämta den senaste versionen av dina data måste användaren använda knappen **Uppdatera** på menyfliken **Data**. Och eftersom arbetsboken ansluter till en datauppsättning i Power BI, måste användare som försöker uppdatera arbetsboken logga in i Power BI och installera Excel-uppdateringarna första gången de försöker uppdatera med den här metoden.

Eftersom användarna måste uppdatera datauppsättningen, och uppdatering för externa anslutningar inte stöds i Excel Online, rekommenderar vi att användarna öppnar arbetsboken i skrivbordsversionen av Excel på datorn.

## <a name="troubleshooting"></a>Felsökning
Det kan finnas tillfällen när Analysera i Excel ger ett oväntat resultat eller funktionen inte fungerar som väntat. [Den här sidan innehåller lösningar för vanliga problem när du använder Analysera i Excel](desktop-troubleshooting-analyze-in-excel.md)

## <a name="next-steps"></a>Nästa steg

Följande artiklar kan också vara av intresse för dig:

* [Använd visning av detaljerad information mellan rapporter i Power BI Desktop](../create-reports/desktop-cross-report-drill-through.md)
* [Använda utsnitt i Power BI Desktop](../visuals/power-bi-visualization-slicers.md)



