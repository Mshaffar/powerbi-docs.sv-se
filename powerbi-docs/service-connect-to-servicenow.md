---
title: Anslut till ServiceNow med Power BI
description: "ServiceNow för Power BI"
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
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: a0dec79f1ecb0aea1f13ff81303183242aceab9d
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-servicenow-with-power-bi-for-incident-reporting"></a>Anslut till ServiceNow med Power BI för rapportering av incidenter
ServiceNow erbjuder flera produkter och lösningar inklusive företag, åtgärder och IT-hantering för att förbättra din verksamhet. Det här innehållspaketet innehåller flera rapporter och insikter om dina öppna, nyligen lösta och nyligen stängda incidenter.  

Anslut till Power BI-innehållspaketet för [ServiceNow Incidents](https://app.powerbi.com/getdata/services/servicenow).

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.
   
   ![](media/service-connect-to-servicenow/pbi_getdata.png) 
2. I rutan **Tjänster** väljer du **Hämta**.
   
   ![](media/service-connect-to-servicenow/pbi_getservices.png) 
3. Välj **ServiceNow Incidents** \> **Hämta**.
   
   ![](media/service-connect-to-servicenow/connect.png)
4. Ange URL:en för din ServiceNow-instans och antalet dagar/poster att hämta in. Observera att så fort du uppnår en gräns så stoppas importen.
   
   ![](media/service-connect-to-servicenow/params.png)
5. När du uppmanas till det, anger du dina autentiseringsuppgifter för ServiceNow **Basic**. Observera att enkel inloggning inte stöds idag, mer information om systemkraven nedan.
   
   ![](media/service-connect-to-servicenow/creds.png)
6. När inloggningsflödet har slutförts startar importprocessen. När den är klar visas en ny instrumentpanel, rapport och modell i navigeringsfönstret. Välj instrumentpanelen för att visa dina importerade data.
   
    ![](media/service-connect-to-servicenow/dashboard.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](service-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](service-dashboard-tiles.md) för att öppna den underliggande rapporten.
* Även om din datauppsättning är schemalagd för att uppdateras dagligen, kan du ändra uppdateringsschemat eller försöka uppdatera den på begäran med **Uppdatera nu**.

## <a name="system-requirements"></a>Systemkrav
För att ansluta behöver du:  

* Ett konto som kan komma åt yourorganization.service-now.com med Basic-autentisering (enkel inloggning stöds inte i den här versionen)  
* Kontot måste ha rest_service-rollen och läsbehörighet till incidenttabellen  

## <a name="troubleshooting"></a>Felsökning
Om du påträffar ett autentiseringsfel vid inläsningen, granska åtkomstkraven ovan. Om du har rätt behörigheter och fortfarande stöter på problem, kan du prata med din ServiceNow-administratör för att kontrollera att du har de ytterligare behörigheter som krävs för din anpassade instans.

Om det uppstår långa laddningstider, kan du granska antalet incidenter och antalet dagar som du angav under anslutningen och överväga att minska dem.

## <a name="next-steps"></a>Nästa steg
[Kom igång med Power BI](service-get-started.md)

[Power BI – grundläggande begrepp](service-basic-concepts.md)
