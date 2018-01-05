---
title: "Så här uppdaterar du dina innehållspaketautentiseringsuppgifter för Xero"
description: "Om du använder Xero Power BI-innehållspaketet kan du ha stött på ett problem med innehållspaketets dagliga uppdateringar på grund av en nyligen inträffad incident i Power BI-tjänsten."
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/10/2017
ms.author: yshoukry
ms.openlocfilehash: 1546d9274a0c838dc763658853913208f340bb27
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2017
---
# <a name="how-to-refresh-your-xero-content-pack-credentials-if-refresh-failed"></a>Så här uppdaterar du dina innehållspaketautentiseringsuppgifter för Xero om uppdateringen misslyckades
Om du använder Xero Power BI-innehållspaketet kan du ha stött på problem med innehållspaketets dagliga uppdateringar på grund av en nyligen inträffad incident i Power BI-tjänsten.

Du kan se om ditt innehållspaket har uppdaterats genom att kontrollera den senaste uppdateringsstatusen för din Xero-datauppsättning som visas på skärmbilden nedan.

![](media/service-refresh-xero-credentials/powerbi-xero-refresh-failed.png)

Om du ser att uppdateringen har misslyckats, så förnya ditt innehållspakets autentiseringsuppgifter genom att följa dessa steg.

1. Klicka på ellipsen (...) bredvid Xero-datauppsättningen, och klicka sedan på **Schemauppdatering**. Då öppnas inställningssidan för Xero-innehållspaketet.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-schedule-refresh.png)
2. Välj **Datakällans autentiseringsuppgifter** > **Redigera autentiseringsuppgifter** på sidan **Inställningar för Xero**.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-settings-page.png)
3. Ange ditt organisationsnamn > **Nästa**.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-configure.png)
4. Logga in med ditt Xero-konto.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-welcome.png)
5. Nu när dina autentiseringsuppgifter har uppdaterats, så kontrollera att uppdateringsschemat är inställt på att köras varje dag. Kontrollera detta genom att klicka på ellipsen (...) bredvid Xero-datauppsättningen, och sedan klicka på **Schemauppdatering** igen.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-refresh-schedule.png)
6. Du kan också välja att uppdatera datauppsättningen direkt. Klicka på ellipsen (...) bredvid Xero-datauppsättningen, och klicka sedan på **Uppdatera nu**.
   
    ![](media/service-refresh-xero-credentials/powerbi-xero-refresh-now.png)

Om du fortfarande har uppdateringsproblem så tveka inte att kontakta oss på [http://support.powerbi.com](http://support.powerbi.com) 

Om du vill veta mer om Xero-innehållspaketet för Power BI kan du besöka hjälpsidan för [Xero-innehållspaket](service-connect-to-xero.md).

### <a name="next-steps"></a>Nästa steg
* Har du fler frågor? [Försök med att fråga Power BI Community](http://community.powerbi.com/)
