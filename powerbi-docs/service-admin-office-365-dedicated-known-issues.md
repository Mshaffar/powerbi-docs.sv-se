---
title: "Office 365-dedikerade kunder – kända problem"
description: "Support för Office 365-dedikerade kunder – kända problem. I det här avsnittet beskrivs problem som är specifika för en Office 365-dedikerad kund. Detta innefattar begränsningar i gruppfunktionen samt iPhone-appen med anpassade domäner."
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
ms.date: 06/28/2017
ms.author: asaxton
ms.openlocfilehash: 8ee54e64ecbb72354a70a2aeb1d8fda87b3b876b
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/13/2017
---
# <a name="office-365-dedicated-customers---known-issues"></a>Office 365-dedikerade kunder – kända problem
Power BI har nu stöd för Office 365-dedikerade kunder.  Om du är en O365-dedikerad kund kan du logga in med ett konto från den klienten och använda Power BI. Det finns för närvarande två kända problem.

## <a name="groups"></a>Grupper
När du väljer **Medlemmar** eller **Kalender** i snabbmenyn Grupp omdirigeras du till e-postappen i stället.  **Filer** och **Konversationer** fungerar som förväntat.

![](media/service-admin-office-365-dedicated-known-issues/group-menu.png)

## <a name="iphone-app---sign-in-with-vanity-domain-leads-to-error"></a>iPhone-app – Inloggning med en anpassad domän leder till fel
När du loggar in på iPhone-appen med en anpassad domän kan det uppstå ett fel.

*Inloggningsfel*  
*Ett oväntat internt fel har uppstått. Försök igen.*

Undvik problemet genom att logga in med e-postadressen som visas när du klickar på användarikonen i Power BI-tjänsten, i stället för med den anpassade domänen.

![](media/service-admin-office-365-dedicated-known-issues/sign-in-address.png)

Har du fler frågor? [Försök med att fråga Power BI Community](http://community.powerbi.com/)
