---
title: Redigera parameterinställningar i Power BI-tjänsten
description: Frågeparametrar skapas i Power BI Desktop men kan granskas och uppdateras i Power BI-tjänsten
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 11/21/2018
ms.author: maggies
LocalizationGroup: Create reports
ms.openlocfilehash: 9dad3e306f895e8c8bf2930b8e032ec558f3f7fc
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/13/2020
ms.locfileid: "83308358"
---
# <a name="edit-parameter-settings-in-the-power-bi-service"></a>Redigera parameterinställningar i Power BI-tjänsten
Rapportskapare lägger till i frågeparametrar till rapporter i Power BI Desktop. Med parametrar kan de göra så att delar av en rapport är beroende av en eller flera *parametervärden*. Rapportens skapare kan till exempel skapa en parameter som begränsar data till ett land/en region, eller en parameter som definierar godkända format för fält som datum, tid och text.

![Start-fliken med alternativet Hantera parametrar i Desktop](media/service-parameters/power-bi-manage-parameters.png)

## <a name="review-and-edit-parameters-in-power-bi-service"></a>Granska och redigera parametrar i Power BI-tjänsten

Som rapportskapare definierar du parametrar i Desktop. När du [publicerar rapporten till Power BI-tjänsten](../create-reports/desktop-upload-desktop-files.md) flyttas parameterinställningar och val med den. Du kan granska och redigera vissa parameterinställningar i Power BI-tjänsten – inte parametrar som begränsar tillgängliga data, men däremot de parametrar som definierar och beskriver godkända värden.

1. Välj kugghjulsikonen i Power BI-tjänsten ![kugghjulsikon](media/service-parameters/power-bi-cog.png) för att öppna **Inställningar**.

2. Välj fliken **Datauppsättningar** och markera en datauppsättning i listan. 
    
    ![Fönstret Inställningar med fliken Datauppsättningar markerad](media/service-parameters/power-bi-select-dataset2.png)

3. Expandera **Parametrar**.  Om den valda datauppsättningen inte har några parametrar, visas ett meddelande med en länk till mer information om frågeparametrar. Om datauppsättningen har parametrar visas dessa när rubriken **Parametrar** expanderas. 

    ![Fönstret Inställningar med Parametrar expanderat](media/service-parameters/power-bi-settings.png)

    Granska parameterinställningarna och gör ändringar om det behövs. Gråtonade fält kan inte redigeras. 


## <a name="next-steps"></a>Nästa steg
Ett ad hoc-sätt att lägga till enkla parametrar är att [ändra URL:en](../collaborate-share/service-url-filters.md).