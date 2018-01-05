---
title: "Fästa en hel rapportsida på en Power BI-instrumentpanel "
description: "Dokumentation om hur du kan fästa en hel liverapportsida på en Power BI-instrumentpanel från en rapport."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: ee8e7541db7f40a5d01607c6551ee734eb9f3d5b
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/13/2017
---
# <a name="pin-an-entire-report-page-as-a-live-tile-to-a-power-bi-dashboard"></a>Fästa en hel rapportsida, som en levande panel, på en Power BI-instrumentpanel
Ett annat sätt att lägga till en ny [instrumentpanelspanel](service-dashboard-tiles.md) är genom att fästa en rapportsida.  Detta är ett enkelt sätt att fästa flera visualiseringar åt gången.  När du fäster en hel sida är panelerna dessutom *live*. Du kan interagera med dem direkt på instrumentpanelen. Ändringar du gör i någon av visualiseringarna i rapportredigeraren, om du till exempel lägger till ett filter eller ändrar fälten som används i diagrammet, visas då även på instrumentpanelen.  

> [!NOTE]
> Du kan fästa paneler från rapporter som delas med dig.
> 
> 

## <a name="pin-a-report-page"></a>Fäst en rapportsida
Se hur Amanda fäster en liverapportsida på en instrumentpanel och följ sedan de stegvisa anvisningarna under videon och prova själv.

<iframe width="560" height="315" src="https://www.youtube.com/embed/EzhfBpPboPA" frameborder="0" allowfullscreen></iframe>


1. Öppna en rapport i [redigeringsvyn](service-interact-with-a-report-in-editing-view.md).
2. Välj **Fäst Live-sida** på menyraden när inga visualiseringar har markerats.
   
   ![](media/service-dashboard-pin-live-tile-from-report/pbi-pin-live-page.png) 
3. Fäst panelen på en befintlig eller ny instrumentpanel. Lägg märke till den markerade texten: *Fäst Live-sida möjliggör att ändringar som görs i rapporterna visas på instrumentpanelen när sidan uppdateras.*
   
   * Befintlig instrumentpanel: välj instrumentpanelens namn i listrutan. Instrumentpaneler som har delats med dig visas inte i listrutan.
   * Ny instrumentpanel: Skriv instrumentpanelens namn.
     
     ![](media/service-dashboard-pin-live-tile-from-report/pbi-pin-live-page-dialog.png)
4. Välj **Fäst live**. Genom ett meddelande (nära det övre högra hörnet) får du reda på att sidan har lagts till, som ett fönster, på instrumentpanelen.

## <a name="open-the-dashboard-to-see-the-pinned-live-tile"></a>Öppna instrumentpanelen om du vill se den fästa levande panelen
1. Välj instrumentpanelen med den nya levande panelen i navigeringsfönstret. Där kan du göra sådant som att [byta namn på, ändra storlek på, länka och flytta](service-dashboard-edit-tile.md) den fästa rapportsidan.  
2. Interagera med den levande panelen.  I skärmbilden nedan har en stapel i kolumndiagrammet markerats, varvid de övriga visualiseringarna på panelen har korsfiltrerats och korsmarkerats.
   
    ![](media/service-dashboard-pin-live-tile-from-report/pbi-live-tile.png)

## <a name="next-steps"></a>Nästa steg
[Instrumentpaneler i Power BI](service-dashboards.md)

Har du fler frågor? [Försök med att fråga Power BI Community](http://community.powerbi.com/)
