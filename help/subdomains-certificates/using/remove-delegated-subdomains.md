---
product: campaign
solution: Campaign
title: Delegatie van subdomeinen verwijderen
description: Leer hoe u het delegeren van subdomeinen naar Adobe kunt verwijderen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 5a8c4c4d1c5c527135901cd41f2b0936af8737b4
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 1%

---

# Delegatie van subdomeinen naar Adobe verwijderen {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Subdomeindelegatie verwijderen"
>abstract="In dit scherm kunt u de delegatie van een subdomein naar Adobe verwijderen. Houd er rekening mee dat dit proces na verzending niet kan worden teruggedraaid of gestopt.<br><br>Als u de delegatie van een primair domein voor de geselecteerde instantie probeert te verwijderen, wordt u gevraagd het domein te kiezen dat het zal vervangen."

Met het Configuratiescherm kunt u de delegatie verwijderen van een subdomein dat is gedelegeerd aan Adobe, inclusief CNAME-instelling.

## Belangrijke opmerkingen {#important}

Overweeg voordat u verdergaat zorgvuldig de effecten die optreden wanneer het verwijderingsproces wordt gestart:

* Verwijderen van subdomeindelegatie kan niet ongedaan worden gemaakt en is onomkeerbaar zodra dit is gestart totdat het proces wordt uitgevoerd.
* Geen andere subdomeindelegatie kan worden verwijderd wanneer een gelijkaardig proces op een ander subdomein lopend is.
* Een delegatie die op een subdomein is verwijderd, kan pas drie dagen na verwijdering opnieuw worden gedelegeerd.

## Een subdomeindelegatie verwijderen {#steps}

Voer de volgende stappen uit om het delegeren van een subdomein naar Adobe te verwijderen:

1. Klik op de knop Ovaal naast de domeindelegatie die u wilt verwijderen en selecteer deze **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. Herzie de disclaimer en erken de verwijdering van de domeindelegatie naar Adobe.

1. Informatie van het overzicht betreffende de instantie waaraan subdomain wordt geassocieerd, met inbegrip van verwante IP affiniteiten en merkconfiguraties.

   Als u de delegatie van het primaire domein voor de geselecteerde instantie verwijdert, moet u het domein kiezen dat het gebruikend zal vervangen **[!UICONTROL Replacement Domain]** lijst.

   Klikken **[!UICONTROL Next]** om verder te gaan met de verwijdering.

   ![](assets/undelegate-subdomain-details.png)

1. Controleer het overzicht dat wordt weergegeven. Om de verwijdering te bevestigen, typ URL van het domein waarvoor u de delegatie wilt verwijderen en klik **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

Nadat het delegeren is begonnen, toont de hangende baan in de baanlogboeken tot het wordt voltooid.

![](assets/undelegate-job.png)

## Foutcodes {#FAQ}

In deze sectie worden de foutberichten weergegeven die kunnen optreden wanneer u probeert de delegatie van een subdomein te verwijderen:

| Foutcode | Bericht | Beschrijving |
|  ---  |  ---  |  ---  |
| 8002 | Aangevraagde gedelegeerde domein-verwijdering kan niet worden opgelost omdat er een vergelijkbare overlappende aanvraag in uitvoering is. Probeer het na 3 dagen | Een verwijdertaak voor subdomeindelegatie wordt al uitgevoerd voor de geselecteerde instantie. Wacht tot 3 dagen om een nieuwe verwijdertaak te starten. |
| 8003 | Verwijderen van gezochte gedelegeerde domeinen wordt voor dit exemplaar niet ondersteund. | Het verwijderen van delegaties wordt niet ondersteund voor het geselecteerde subdomein vanwege een technisch probleem. Neem contact op met de klantenservice. |
| 8004 | Aangevraagde verwijdering van gedelegeerde domein is niet toegestaan omdat er in dit geval slechts één domein is. | Er is slechts één subdomein gedelegeerd voor de geselecteerde instantie. Verwijderen van delegatie is niet toegestaan. |
| 8005 | De gevraagde Verwijdering van Gedelegeerde Domein wordt niet gesteund voor deze configuratie. | Het verwijderen van delegaties wordt niet ondersteund voor het geselecteerde subdomein vanwege een technisch probleem. Neem contact op met de klantenservice. |
| 8006 | Gevraagde verwijdering van gedelegeerde domeinen is niet toegestaan vanwege onbekende redenen. Neem contact op met de klantenservice. | Het verwijderen van delegaties wordt niet ondersteund voor het geselecteerde exemplaar vanwege onbekende problemen. Neem contact op met de klantenservice. |
