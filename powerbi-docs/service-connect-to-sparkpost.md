---
title: Anslut till SparkPost med Power BI
description: "SparkPost för Power BI"
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
ms.openlocfilehash: 93d124bef56bbb6aeb266844e9b3b633df057fa0
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-sparkpost-with-power-bi"></a>Anslut till SparkPost med Power BI
Power BI-innehållspaketet för SparkPost låter dig extrahera värdefulla datauppsättningar från ditt SparkPost-konto i en insiktsfull instrumentpanelen. Med SparkPost-innehållspaketet kan du visualisera din totala e-poststatistik, inklusive domäner, kampanjer och engagemang efter Internetleverantör.

Anslut till [SparkPost-innehållspaketet](https://app.powerbi.com/getdata/services/spark-post) för Power BI.

## <a name="how-to-connect"></a>Så här ansluter du
1. Välj **Hämta data** längst ned i det vänstra navigeringsfönstret.
   
   ![](media/service-connect-to-sparkpost/getdata.png)
2. I rutan **tjänster** väljer du **Hämta**.
   
   ![](media/service-connect-to-sparkpost/services.png)
3. Välj **SparkPost**-innehållspaketet och klicka på **hämta**. 
   
   ![](media/service-connect-to-sparkpost/sparkpost.png)
4. Ange din SparkPost API-nyckel och välj logga in när du ombeds. Visa information om [hitta de här parametrarna](#FindingParams) nedan.
   
   ![](media/service-connect-to-sparkpost/creds.png)
5. Dina data börjar läsa in beroende på storleken på kontot, detta kan ta en stund. När Power BI har importerat data visas en ny instrumentpanel, rapport och datauppsättning i det vänstra navigeringsfönstret, ifyllt med din e-poststatistik för de senaste 90 dagarna. Nya objekt markeras med en gul asterisk \*.
   
   ![](media/service-connect-to-sparkpost/dashboard.png)

**Och sedan?**

* Prova att [ställa en fråga i rutan Frågor och svar](service-q-and-a.md) överst på instrumentpanelen
* [Ändra panelerna](service-dashboard-edit-tile.md) på instrumentpanelen.
* [Välj en panel](service-dashboard-tiles.md) för att öppna den underliggande rapporten.
* Även om din datauppsättning kommer att vara schemalagd att uppdateras dagligen, kan du ändra uppdateringsschemat eller uppdatera på begäran med **Uppdatera nu**

## <a name="whats-included"></a>Vad ingår
SparkPost-innehållspaketet för Power BI innehåller information, bland annat unika klick, godkända priser, acceptansfrekvens, fördröjningsfrekvens, avvisningsfrekvens och mycket mer.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Hitta parametrar
Innehållspaketet använder en API-nyckel för att ansluta ditt SparkPost-konto till Power BI. Du hittar din API-nyckel i ditt konto under konto \> API & SMTP (mer information [här](https://support.sparkpost.com/customer/portal/articles/1933377-create-api-keys)). Vi föreslår att du använder en API-nyckel med behörigheter för `Message Events: Read-only `och `Metrics: Read-only`

![](media/service-connect-to-sparkpost/sparkpost1.png)
