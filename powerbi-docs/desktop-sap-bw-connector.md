---
title: "Använd anslutningstjänsten SAP BW i Power BI Desktop"
description: "Använd anslutningstjänsten SAP BW i Power BI Desktop"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 13f6a3fa5fc5ae5c2bea2fb6b91250216eebcc01
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/06/2017
---
# <a name="use-the-sap-bw-connector-in-power-bi-desktop"></a>Använd anslutningstjänsten SAP BW i Power BI Desktop
Med Power BI Desktop kan du komma åt **SAP BusinessWarehouse (BW)**-data.

## <a name="installation-of-sap-bw-connector"></a>Installationen av SAP BW-anslutningsappen
För att använda anslutningsappen **SAP BW Connector** ska du utföra följande installationssteg:

1. Installera **SAP NetWeaver**-biblioteket på din lokala dator. Du kan hämta biblioteket **SAP Netweaver** från SAP-administratören eller direkt från [SAP Software Download Center](https://support.sap.com/swdc). Eftersom **SAP Software Download Center** ofta ändrar struktur, finns det inte tydligare riktlinjer för att navigera den webbplatsen. Biblioteket **SAP NetWeaver** ingår vanligtvis också i installationen av klientverktyg för SAP.
   
   Det kan vara möjligt att söka efter *SAP Note #1025361* för att hitta hämtningsplatsen för den senaste versionen. Se till att arkitekturen för **SAP NetWeaver**-biblioteket (32-bitars eller 64-bitars) matchar din installation av **Power BI Desktop** och installera alla filer som ingår i **SAP NetWeaver RFC-SDK**  enligt SAP Note.
2. Dialogrutan **Hämta data** innehåller en post för **SAP Business Warehouse Server** i kategorin **Databas**.
   
   ![](media/desktop-sap-bw-connector/sap_bw_2a.png)

## <a name="sap-bw-connector-features"></a>Funktioner för SAP BW-anslutningsappen
Förhandsversionen av anslutningsappen **SAP BW** i Power BI Desktop låter användare importera data från sina **SAP Business Warehouse Server**-kuber. Du kan också använda DirectQuery med anslutningsappen **SAP BW**. Du måste ange *Server*, *Systemnummer* och *klient-ID* för att upprätta anslutningen.

![](media/desktop-sap-bw-connector/sap_bw_3a.png)

Du kan också ange ytterligare två **avancerade alternativ**: språkkod och ett anpassat MDX-uttryck som ska köras mot den angivna servern.

![](media/desktop-sap-bw-connector/sap_bw_4a.png)

Om inget MDX-uttryck har angetts visas fönstret **Navigator** med en lista med kuber som är tillgängliga i servern, ett alternativ för att ser mer information och välja objekt från tillgängliga kuber, inklusive dimensioner, samt åtgärder. Power BI exponerar frågor och kuber som exponeras av BAPI:et [BW Open Analysis Interface OLAP](https://help.sap.com/saphelp_nw70/helpdata/en/d9/ed8c3c59021315e10000000a114084/content.htm).

När du markerar en eller flera objekt från servern skapas en förhandsgranskning av utdatatabellen baserat ditt val.

![](media/desktop-sap-bw-connector/sap_bw_5.png)

Fönstret **Navigator** innehåller också några **Visningsalternativ** som gör det möjligt att göra följande:

* **Visa *endast valda objekt* jämfört med *alla objekt* (standardvy):** det här alternativet är användbart för att verifiera den slutgiltiga objektuppsättningen. En annan metod för att visa detta är att välja *kolumnnamn* i området *Förhandsvisning*.
* **Aktivera förhandsgranskningar av data (standardinställning):** du kan också styra om förhandsgranskade data ska visas i den här dialogrutan. Om du inaktiverar förhandsgranskningar av data minskar mängden serveranrop eftersom data inte längre begärs för förhandsgranskning.
* **Tekniska namn:** SAP BW stöder begreppet *Tekniska namn* för objekt i en kub. Med tekniska namn kan en kubägare exponera ett *användarvänligt* namn för kubobjekt, till skillnad från endast det *fysiska namnet* för objekten i kuben.

![](media/desktop-sap-bw-connector/sap_bw_6.png)

När du har valt alla nödvändiga objekt i **Navigatorn** kan du bestämma vad du ska göra genom att välja någon av följande knappar längst ned på fönstret **Navigator**:

* När du väljer **Hämta** läses hela uppsättningen rader för utdatatabellen i Power BI Desktop-datamodellen in. Du leds sedan till **rapport**vyn där du kan börja visualisera dina data eller göra ytterligare ändringar med hjälp av vyerna **Data** eller **Relationer**.
* Genom att välja **Redigera** öppnas **Frågeredigeraren** där du kan transformera och filtrera dina data ytterligare innan hela uppsättningen rader hämtas till Power BI Desktop-datamodellen.

Förutom att importera data från **SAP BW**-kuber, kom ihåg att du även kan importera data från en mängd andra datakällor i Power BI Desktop och sedan kombinera dem i samma rapport. Detta ger alla möjliga sorters intressanta scenarier för rapportering och analys utöver **SAP BW**-data.

## <a name="troubleshooting"></a>Felsökning
Det här avsnittet innehåller felsökningssituationer (och lösningar) för arbete med den här förhandsversionen av anslutningsappen **SAP BW**.

1. Numeriska data från **SAP BW** returnerar punkter i stället för blanksteg som decimaltecken. Till exempel returneras 1 000 000 som 1.000.000.
   
   **SAP BW** returnerar decimaldata med antingen ett *,* (komma) eller en *.* (punkt) som decimaltecken. För att ange vilka av dessa som **SAP BW** ska använda som decimalavgränsare anropar drivrutinen för **Power BI Desktop** *BAPI_USER_GET_DETAIL*. Det här anropet returnerar en struktur som kallas **DEFAULTS**, som har ett fält med namnet *DCPFM* som lagrar *formatet för decimaltecken*. Det antar ett av följande tre värden:
   
       ‘ ‘ (space) = Decimal point is comma: N.NNN,NN
       'X' = Decimal point is period: N,NNN.NN
       'Y' = Decimal point is N NNN NNN,NN
   
   Kunder som har rapporterat problemet upptäcktes att anropet till *BAPI_USER_GET_DETAIL* misslyckas för en viss användare (användaren som visar felaktiga data), med ett felmeddelande som liknar följande:
   
       You are not authorized to display users in group TI:
           <item>
               <TYPE>E</TYPE>
               <ID>01</ID>
               <NUMBER>512</NUMBER>
               <MESSAGE>You are not authorized to display users in group TI</MESSAGE>
               <LOG_NO/>
               <LOG_MSG_NO>000000</LOG_MSG_NO>
               <MESSAGE_V1>TI</MESSAGE_V1>
               <MESSAGE_V2/>
               <MESSAGE_V3/>
               <MESSAGE_V4/>
               <PARAMETER/>
               <ROW>0</ROW>
               <FIELD>BNAME</FIELD>
               <SYSTEM>CLNTPW1400</SYSTEM>
           </item>
   
   Om du vill lösa det här felet måste användarna be sina SAP-administratör att ge SAPBW-användaren som används i Power BI behörighet för att köra *BAPI_USER_GET_DETAIL*. Det är också värt att kontrollera att användaren har det nödvändiga *DCPFM*-värdet, enligt föregående beskrivning i den här felsökningen.
2. **Anslutning för SAP BEx-frågor**
   
   Du kan utföra **BEx**-frågor i Power BI Desktop genom att aktivera en specifik egenskap, enligt följande bild:
   
   ![](media/desktop-sap-bw-connector/sap_bw_8.png)
