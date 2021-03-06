---
title: Ändringslogg för API för visuella Power BI-objekt
description: Den här artikeln beskriver huvudsakliga ändringar i olika versioner av API för visuella Power BI-objekt
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 03/13/2019
ms.openlocfilehash: fa8759d7edb519240140263bcd01bfdddd9c7d86
ms.sourcegitcommit: bfc2baf862aade6873501566f13c744efdd146f3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/13/2020
ms.locfileid: "83141062"
---
# <a name="power-bi-visuals-api-changelog"></a>Ändringslogg för API för visuella Power BI-objekt
Den här sidan innehåller en snabböversikt över API-versionerna. Versioner som anges här betraktas som stabila och kommer inte att ändras.

## <a name="api-v26"></a>API v2.6
  * Lägger till **isInFocus** till alternativet Uppdatera och **switchFocusModeState**-metoden till visuell värd
  * Stöder **delsummor**-anpassning

## <a name="api-v25"></a>API v2.5
  * Stöder **[Fönstret Analys](./analytics-pane.md)**
  * Stöder metoderna `SelectionIdBuilder`**withMatrixNode** och **withTable**
  * Har inte längre stöd för `DataRepetitionSelector`-gränssnittet, ersatt med `data.CustomVisualOpaqueIdentity`-gränssnittet

## <a name="api-v23"></a>API v2.3
  * **[API för Landningssida](./landing-page.md)**
  * **[API för lokal lagring](./local-storage.md)**
  * **[API för tuppelfilter (flerkolumnsfilter)](./filter-api.md#the-tuple-filter-api-multi-column-filter)**
  * **[API för rendering av händelser](./event-service.md#render-events-in-power-bi-visuals)**

## <a name="api-v22"></a>API v2.2
  * Stöder **[återställning av JSON-filter från DataView](./filter-api.md#restore-the-json-filter-from-the-data-view)**
  * **[ContextMenu API](./context-menu.md)**

## <a name="api-v21"></a>API v2.1
  * Prestandaförbättringar:
    * Snabbare inläsningstider
    * Mindre minnesstorlek
    * Optimerade data- och händelsetransaktioner  

**Viktig information**
* Omstrukturerade filtrerings-API:er finns tillgängliga i API 2.2 och stöds inte i API 2.1.
* Visuella objekt tar bara emot den dataView-typ som har deklarerats i deras funktioner. Visuella objekt som använder flera dataView-typer kommer att sluta fungera till följd av den här uppdateringen.
* Har inte längre stöd för `DataViewScopeIdentity`-gränssnittet, ersatt med `data.DataRepetitionSelector`-gränssnittet. Om du har använt nyckelegenskapen i `DataViewScopeIdentity`-gränssnittet kan du ersätta den med `JSON.stringify(identity)`
* `undefined` ersätts med `null` inuti dataView. När du itererar över en matris med `var item in myArray` hoppar den över `undefined`, men hoppar inte över `null`. Visuella objekt som använder det här mönstret kan sluta fungera med den här uppdateringen. Se till att söka efter `null` i matriser:
   ```typescript
   for (var item in myArray) {
     if (!item) {
       continue;
     }
     console.log(item);
   }
   ```
* Egenskapen `proto` lagrar inte längre dolda metadata\data i dataView. Visuella objekt med som kommer åt egenskaper via `proto` kan sluta fungera med den här uppdateringen.

## <a name="api-v113"></a>API v1.13
* Stöder **[Sync-utsnitt](./enable-sync-slicers.md)** , observera att detta endast fungerar för enskilda fältutsnitt på grund av PBI aktuellt kodtillstånd [läs mer](/power-bi/desktop-slicers).
* Tillgänglighet: [Högkontraststöd](./high-contrast-support.md) 
* Tillgänglighet: Tillåt tangentbordsfokusflagga

## <a name="api-v112"></a>API v1.12
* Stöder teman
* Har stöd för **[fetchMoreData](./fetch-more-data.md)** , observera att **Hämta mer data-API:t** överkommer den hårda gränsen på 30 000 datapunkter
* **[API för arbetsytans knappbeskrivningar](./add-tooltips.md#add-report-page-tooltips)**

## <a name="api-v111"></a>API v1.11
* **[FilterManager API](./filter-api.md)**
* Stöder **[bokmärken](./bookmarks-support.md)** 

## <a name="api-v110"></a>API v1.10
* Lägger till `ILocalizationManager`
* **API för autentisering**

## <a name="api-v19"></a>API v1.9
* **[launchUrl API](./launch-url.md)**

## <a name="api-v18"></a>API v1.8
* Stöder den nya typen **fillRule** (toning) i funktionsschemat
* Stöder **regel**-egenskapen i funktionsschemat för objektegenskaper

## <a name="api-v17"></a>API v1.7
* Stöder **[RESJSON](./localization.md#resource-file)**

## <a name="api-v162"></a>API v1.6.2
* Stöder **[Redigeringsläge](./advanced-edit-mode.md)** för visuella objekt för att komma in i visuellt redigeringsläge
* Stöder **[Interaktiv (HTML) visuella R Power BI-objekt](https://microsoft.github.io/PowerBI-visuals/tutorials/building-r-powered-custom-visual/creating-r-visuals.md)** , baserat på HTML

## <a name="api-v150"></a>API v1.5.0
* Stöder **[Tillåt interaktioner](./visuals-interactions.md)** för visuell interaktivitet

## <a name="api-v140"></a>API v1.4.0
* Stöder **[Lokalisering](./localization.md)**

## <a name="api-v130"></a>API v1.3.0
* Stöder **[Knappbeskrivningar](./add-tooltips.md)**

## <a name="api-v120"></a>API v1.2.0
* Lägger till **colorPalette** för att hantera de färger som används i ditt visuella objekt.
* Stöder **Markering av flera** – selectionManager kan acceptera en matris med `SelectionId`.
* Stöder **[visuella R-objekt](https://microsoft.github.io/PowerBI-visuals/tutorials/building-r-powered-custom-visual/creating-r-visuals.md)** med R-skript

## <a name="api-v110"></a>API v1.1.0
* Stöder visuella felsökningsobjekt i iFrame
* Lägger till begränsat läge för låg vikt med snabbare initiering av iFrame
* Åtgärdar [Capabilities.objects stöder inte text-typ](https://github.com/Microsoft/PowerBI-visuals-tools/issues/12) problem
* Stöder `pbiviz update` att uppdatera Visual API Type-definitioner och schema
* Stöder `--api-version` flagga i `pbiviz new` för att skapa visuella objekt med en särskild API-version
* Stöder alfaversionen av API v1.2.0

**Visuell värd**
* Lägger till **createSelectionIdBuilder** för att skapa unika identifierare som används för dataurval
* Lägger till **createSelectionManager** för att hantera markeringsstatus för det visuella objektet och kommunicerar ändringar i den visuella värden
* Lägger till en matris med standard **färger** som ska användas i visuella objekt

## <a name="api-v100"></a>API v1.0.0
* Initial API-version
