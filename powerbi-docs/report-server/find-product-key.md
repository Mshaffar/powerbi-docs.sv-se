---
title: "Så här hittar du rapportserverns produktnyckel"
description: "Lär dig hur du hittar produktnyckeln för Power BI-rapportservern för att installera servern i en produktionsmiljö."
services: powerbi
documentationcenter: 
author: guyinacube
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 11/01/2017
ms.author: asaxton
ms.openlocfilehash: 64bf842bec0598210e54d73ee2697586fce96a1f
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/13/2017
---
# <a name="how-to-find-your-report-server-product-key"></a>Så här hittar du rapportserverns produktnyckel
Lär dig hur du hittar produktnyckeln för Power BI-rapportservern för att installera servern i en produktionsmiljö.

<iframe width="640" height="360" src="https://www.youtube.com/embed/6CQnf-NGtpU?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

Du har hämtat Power BI-rapportservern och du har ett SQL Server Enterprise Software Assurance-avtal. Eller också har du köpt Power BI Premium. Du vill installera servern i en produktionsmiljö, men du behöver en produktnyckel för att göra det. Var finns produktnyckeln? 

Produktnyckeln ska finnas på någon av följande platser, beroende på vad du har köpt.

## <a name="purchased-power-bi-premium"></a>Om du har köpt Power BI Premium
Om du har köpt Power BI Premium så kommer du att ha tillgång till din produktnyckel för Power BI-raportservern i fliken **kapacitetsinställningar** i Power BI-administratörsportalen. Den finns endast tillgänglig för globala administratörer eller användare som har tilldelats rollen Power BI-tjänstadministratör.

![Power BI-rapportservernyckeln i premiuminställningarna](media/find-product-key/pbirs-product-key.png)

Om du väljer **Power BI-rapportservernyckel** så visas en dialogruta med din produktnyckel. Du kan kopiera den och använda den med installationen.

![Produktnyckel för Power BI-rapportserver](media/find-product-key/pbirs-product-key-dialog.png)

## <a name="purchased-software-assurance-agreeemnt"></a>Avtal för köpt programvara
Om du har ett SQL Server Enterprise SA-avtal, kan du få din produktnyckel från [Volume Licensing Service Center](https://www.microsoft.com/Licensing/servicecenter/). Titta under det senaste servicepaketet för den senaste versionen av SQL Server. Om du inte ser det, tittar du under RTM-versionen av den senaste versionen av SQL Server.

> [!NOTE]
> Du behöver titta under nedladdningar. Inte avsnittet nycklar.
> 
> 

![](media/find-product-key/vlsc-download.png "Volume Licensing Service Center")

## <a name="next-steps"></a>Nästa steg
[Snabbstart: Installera Power BI-rapportserver](quickstart-install-report-server.md)  
[Installera Power BI Desktop som har optimerats för Power BI-rapportservern](install-powerbi-desktop.md)  
[Installera Report Builder](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Ladda ned SQL Server Data Tools (SSDT)](http://go.microsoft.com/fwlink/?LinkID=616714)

Har du fler frågor? [Fråga Power BI Community](https://community.powerbi.com/)
