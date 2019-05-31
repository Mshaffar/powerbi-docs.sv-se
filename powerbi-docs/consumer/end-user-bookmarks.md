---
title: Översikt över bokmärken i Power BI-Tjänsterapporter
description: Dokumentationsöversikt för Power BI frågor och svar frågor med naturligt språk.
author: mihart
manager: kvivek
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 05/10/2019
ms.author: mihart
LocalizationGroup: Create reports
ms.openlocfilehash: 55fafb00135908dc4f82151b96ed04d2cf2568da
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/29/2019
ms.locfileid: "65608316"
---
# <a name="what-are-bookmarks"></a>Vad är bokmärken?
Bokmärken avbilda konfigurerade visningar av rapportsidan, inklusive filter, utsnitt och tillstånd för visuell information. När du väljer ett bokmärke, kommer Power BI du tillbaka till vyn. Det finns två typer av bokmärken – de som du skapar själv och de som används av rapporten *designers*.

## <a name="use-bookmarks-to-share-insights-and-build-stories-in-power-bi"></a>Använda bokmärken för att dela information och skapa artiklar i Power BI 
Det finns många användningsområden för bokmärken. Anta att du har hittat en intressant insikt och vill bevara den – skapa ett bokmärke så att du kan gå tillbaka senare. Behöva lämna och vill spara din aktuella arbete, skapar ett bokmärke. När du vill skapa ett bokmärke som standardvyn i rapporten, så att varje gång du returnera att visa på rapportsidan öppnas först. 

Du kan också skapa en samling bokmärken, ordna dem i den ordning som du vill ha och sedan gå igenom varje bokmärke i en presentation om du vill markera en serie insikter som berättar en historia.  

![Visa fönstret bokmärken genom att välja den från menyfliksområdet.](media/end-user-bookmarks/power-bi-bookmarks-pane.png)

## <a name="using-bookmarks"></a>Använda bokmärken
Öppna fönstret bokmärken genom att välja **bokmärken** på menyraden. Om du vill återgå till den ursprungliga publicerade vyn i rapporten, Välj **Återställ till standard**.

### <a name="report-bookmarks"></a>Rapporten bokmärken
Om rapporten *designer* ingår rapporten bokmärken, hittar du dem under den **rapportera bokmärken** rubrik. 

![Visa rapporten bokmärken.](media/end-user-bookmarks/power-bi-report-bookmark.png)

Välj ett bokmärke för att ändra till den rapportvyn. 

![Video som visar rapporten bokmärken väljs.](media/end-user-bookmarks/power-bi-bookmarks.gif)

### <a name="personal-bookmarks"></a>Personliga bokmärken

När du skapar ett bokmärke sparas följande element med bokmärket:

* Nuvarande sida
* Filter
* Utsnitt, inklusive utsnittstyp (till exempel listruta eller lista) och utsnittstillstånd
* Tillstånd för markering i visuellt objekt (till exempel filtrering för flera markeringar)
* Sorteringsordning
* Riktning för detaljnivån
* Synlighet (för ett objekt med hjälp av fönstret **Val**)
* Fokus- eller **Spotlight**-lägen för synliga objekt

Konfigurera en rapport som du vill att den ska visas i bokmärket. När du har utformat din rapportsida och visuella objekt väljer du **Lägg till** från fönstret **Bokmärken** om du vill lägga till ett bokmärke. I det här exemplet har vi lagt till några filter för region och datum. 

![Lägg till personliga bokmärken.](media/end-user-bookmarks/power-bi-add-personal.png)

**Power BI** skapar ett bokmärke och ger den ett allmänt namn eller ett namn som du anger. Du kan *Byt namn på*, *ta bort*, eller *uppdatera* ett bokmärke genom att markera ellipsen bredvid bokmärkets namn och välja en åtgärd på menyn som visas.

När du har ett bokmärke kan du visa den genom att helt enkelt välja bokmärket i den **bokmärken** fönstret. 

![Lägg till personliga bokmärken.](media/end-user-bookmarks/power-bi-personal-bookmark.png)


<!--
## Arranging bookmarks
As you create bookmarks, you might find that the order in which you create them isn't necessarily the same order you'd like to present them to your audience. No problem, you can easily rearrange the order of bookmarks.

In the **Bookmarks** pane, simply drag-and-drop bookmarks to change their order, as shown in the following image. The yellow bar between bookmarks designates where the dragged bookmark will be placed.

![Change bookmark order by drag-and-drop](media/desktop-bookmarks/bookmarks_06.png)

The order of your bookmarks can become important when you use the **View** feature of bookmarks, as described in the next section. 

-->

## <a name="bookmarks-as-a-slide-show"></a>Bokmärken som ett bildspel
Om du vill presentera eller visa bokmärken i ordning, Välj **visa** från den **bokmärken** fönstret för att starta ett bildspel.

När du är i **visnings**läget finns det några funktioner att observera:

1. Namnet på bokmärket visas i namnlisten för bokmärket, som visas längst ned i arbetsytan.
2. Namnlistan för bokmärket har pilar som låter dig flytta till nästa eller föregående bokmärke.
3. Du kan avsluta **Visnings**läget genom att välja **Avsluta** från rutan **Bokmärken** eller genom att välja **X** som finns i namnlisten för bokmärket. 

![Lägg till ett bokmärke bildspel](media/end-user-bookmarks/power-bi-bookmark-slideshow.png)

När du är i **Visningsläget** kan du stänga fönstret **Bokmärken** (genom att klicka på X i det här fönstret) för att ge mer utrymme till presentationen. Medan du är i **Visningsläget** är alla visuella objekt interaktiva och är tillgängliga för korsmarkering, precis som de annars skulle vara när du interagerar med dem. 

<!--
## Visibility - using the Selection pane
With the release of bookmarks, the new **Selection** pane is also introduced. The **Selection** pane provides a list of all objects on the current page and allows you to select the object and specify whether a given object is visible. 

![Enable the Selection pane](media/desktop-bookmarks/bookmarks_08.png)

You can select an object using the **Selection** pane. Also, you can toggle whether the object is currently visible by clicking the eye icon to the right of the visual. 

![Selection pane](media/desktop-bookmarks/bookmarks_09.png)

When a bookmark is added, the visible status of each object is also saved based on its setting in the **Selection** pane. 

It's important to note that **slicers** continue to filter a report page, regardless of whether they are visible. As such, you can create many different bookmarks, with different slicer settings, and make a single report page appear very different (and highlight different insights) in various bookmarks.


## Bookmarks for shapes and images
You can also link shapes and images to bookmarks. With this feature, when you click on an object, it will show the bookmark associated with that object. This can be especially useful when working with buttons; you can learn more by reading the article about [using buttons in Power BI](desktop-buttons.md). 

To assign a bookmark to an object, select the object, then expand the **Action** section from the **Format Shape** pane, as shown in the following image.

![Add bookmark link to an object](media/desktop-bookmarks/bookmarks_10.png)

Once you turn the **Action** slider to **On** you can select whether the object is a back button, a bookmark, or a Q&A command. If you select bookmark, you can then select which of your bookmarks the object is linked to.

There are all sorts of interesting things you can do with object-linked bookmarking. You can create a visual table of contents on your report page, or you can provide different views (such as visual types) of the same information, just by clicking on an object.

When you are in editing mode you can use ctrl+click to follow the link, and when not in edit mode, simply click the object to follow the link. 


## Bookmark groups

Beginning with the August 2018 release of **Power BI Desktop**, you can create and use bookmark groups. A bookmark group is a collection of bookmarks that you specify, which can be shown and organized as a group. 

To create a bookmark group, hold down the CTRL key and select the bookmarks you want to include in the group, then click the ellipses beside any of the selected bookmarks, and select **Group** from the menu that appears.

![Create a bookmark group](media/desktop-bookmarks/bookmarks_15.png)

**Power BI Desktop** automatically names the group *Group 1*. Fortunately, you can just double-click on the name and rename it to whatever you want.

![Rename a bookmark group](media/desktop-bookmarks/bookmarks_16.png)

With any bookmark group, clicking on the bookmark group's name only expands or collapses the group of bookmarks, and does not represent a bookmark by itself. 

When using the **View** feature of bookmarks, the following applies:

* If the selected bookmark is in a group when you select **View** from bookmarks, only the bookmarks *in that group* are shown in the viewing session. 

* If the selected bookmark is not in a group, or is on the top level (such as the name of a bookmark group), then all bookmarks for the entire report are played, including bookmarks in any group. 

To ungroup bookmarks, just select any bookmark in a group, click the ellipses, and then select **Ungroup** from the menu that appears. 

![Ungroup a bookmark group](media/desktop-bookmarks/bookmarks_17.png)

Note that selecting **Ungroup** for any bookmark from a group takes all bookmarks out of the group (it deletes the group, but not the bookmarks themselves). So to remove a single bookmark from a group, you need to **Ungroup** any member from that group, which deletes the grouping, then select the members you want in the new group (using CTRL and clicking each bookmark), and select **Group** again. 
-->





## <a name="limitations-and-considerations"></a>Begränsningar och överväganden
Det finns några begränsningar och saker du bör tänka på för den här versionen av **bokmärken**.

* De flesta anpassade visuella objekt bör fungera väl med bokmärkning. Om du stöter på problem med bokmärkning och ett anpassat visuell objekt, kontaktar du den person som skapat det anpassade visuella objektet och ber dem att lägga till stöd för bokmärken till sina visuella objekt. 
* Om du lägger till ett visuellt objekt på en rapportsida efter att du har skapat ett bokmärke kommer det visuella objektet att visas i sitt standardläge. Det innebär att om du lägger till ett utsnitt på en sida där du tidigare skapade bokmärken så fungerar utsnittet i standardtillståndet.
* Flytta runt visuella objekt när ett bokmärke har skapats visas i bokmärket. 
* I allmänhet dina bokmärken påverkas inte om rapporten *designer* uppdaterar eller publicerar rapporten. Men om designern gör större ändringar i rapporten, till exempel ta bort fält som används av ett bokmärke, visas sedan ett felmeddelande visas nästa gång du försöker öppna den bokmärken. 

<!--
## Next steps
spotlight?
-->