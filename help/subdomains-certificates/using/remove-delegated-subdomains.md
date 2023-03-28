---
product: campaign
solution: Campaign
title: Delegatie van subdomeinen verwijderen
description: Leer hoe u de delegatie van subdomeinen aan Adobe kunt verwijderen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: dbd1b2dd31cf732609f8a515e9adc1c43cbf39c6
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 59%

---

# Delegatie van subdomeinen naar Adobe verwijderen {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Subdomeindelegatie verwijderen"
>abstract="In dit scherm kunt u de delegatie van een subdomein aan Adobe verwijderen. Houd er rekening mee dat dit proces niet ongedaan kan worden gemaakt en onomkeerbaar is totdat de uitvoering is voltooid.<br><br>Als u de delegatie van een primair domein voor de geselecteerde instantie probeert te verwijderen, wordt u gevraagd het domein te kiezen dat het gaat vervangen."

Met het Configuratiescherm kunt u de delegatie verwijderen van een subdomein dat volledig is gedelegeerd aan Adobe of gedelegeerd via CNAME&#39;s.

## Belangrijke opmerkingen {#important}

Overweeg zorgvuldig de gevolgen die optreden zodra het verwijderingsproces is gestart, voordat u doorgaat:

* Zodra het proces is geactiveerd, kan de verwijdering van subdomeindelegatie niet ongedaan worden gemaakt en is deze onomkeerbaar totdat de uitvoering van het proces is voltooid.
* Geen enkele andere subdomeindelegatie kan worden verwijderd wanneer een soortgelijk proces op een ander subdomein wordt uitgevoerd.
* Een delegatie die op een subdomein is verwijderd, kan pas 3 dagen na verwijdering opnieuw worden gedelegeerd.

## Een subdomeindelegatie verwijderen {#steps}

Volg deze stappen om de delegatie van een subdomein naar Adobe te verwijderen:

1. Klik op de knop met 3 puntjes naast de domeindelegatie die u wilt verwijderen en selecteer **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. Review de disclaimer en bevestig de verwijdering van de domeindelegatie aan Adobe.

1. Review informatie over de instantie waaraan het subdomein is gekoppeld, inclusief gerelateerde IP-affiniteiten en merkconfiguraties.

   Als u de delegatie van het primaire domein voor de geselecteerde instantie verwijdert, moet u het domein kiezen dat het gaat vervangen met behulp van de lijst **[!UICONTROL Replacement Domain]**.

   Klik op **[!UICONTROL Next]** om door te gaan met verwijderen.

   ![](assets/undelegate-subdomain-details.png)

1. Als u een CNAME-type delegatie verwijdert of als u een primair domein vervangt door een domein dat via CNAME is gedelegeerd, wordt een extra **[!UICONTROL Action]** step-weergaven om DNS-records te beheren. [Meer informatie in deze sectie](#dns)

1. Review het overzicht dat wordt weergegeven. Als u de verwijdering wilt bevestigen, typt u de URL van het domein waarvoor u de delegatie wilt verwijderen en klikt u op **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

Nadat het verwijderen van de delegatie is gestart, wordt de taak in behandeling weergegeven in de taaklogboeken totdat deze is voltooid.

![](assets/undelegate-job.png)

## DNS-recordbeheer {#dns}

Om een domeindelegatie te vormen die CNAMEs gebruikt, vereist het Controlebord dat u specifieke verslagen op uw DNS server toevoegt. [Leer hoe u subdomeinen instelt met gebruik van CNAME&#39;s](setting-up-new-subdomain.md#use-cnames)

Wanneer het verwijderen van een CNAME-type delegatie, moet u **verwijder deze DNS-records** van uw server om problemen te voorkomen. Bovendien, als u de delegatie van primaire subdomain wilt verwijderen en het met een domein vervangen dat gebruikend CNAMEs is afgevaardigd, kunt u moeten **DNS-records toevoegen** op uw server, afhankelijk van de IP eigenschappen die voor subdomain worden geplaatst.

In de onderstaande tabel staan de acties die u wilt uitvoeren, afhankelijk van het type delegatie dat u verwijdert, en het type delegatie dat u hebt gebruikt om het vervangingsdomein in te stellen.

| Verwijderde delegatie | Vervangend domein | Actie vereist |
|  ---  |  ---  |  ---  |
| Volledig | Geen vervangend domein | Geen actie vereist |
| Volledig | CNAME | DNS-records toevoegen (optioneel op basis van de IP-affiniteiten) |
| Volledig | Volledig | Geen actie vereist |
| CNAME | Geen vervangend domein | DNS-records verwijderen |
| CNAME | CNAME | DNS-records verwijderen en toevoegen (optioneel op basis van de IP-affiniteiten) |
| CNAME | Volledig | DNS-records verwijderen |

Hiervoor is een extra **[!DNL Action]** De stappen worden weergegeven voordat de delegatie wordt verwijderd. Dit scherm maakt een lijst van de DNS verslagen om, afhankelijk van de context te verwijderen of toe te voegen.

![](assets/action-step.png)

### DNS-records verwijderen

1. Navigeer naar uw DNS-server en verwijder de records in het Configuratiescherm.
1. Ga terug naar Configuratiescherm en klik op **[!UICONTROL Next]** de delegatie te verwijderen.

### DNS-records toevoegen

1. Navigeer aan uw DNS server en voeg de verslagen toe die in Controlebord worden vermeld.
1. Wacht op de DNS toevoeging om effectief te zijn.
1. Ga terug naar Configuratiescherm en klik op **[!UICONTROL Verify]**.
1. Nadat de toevoeging aan records is geverifieerd, klikt u op **[!UICONTROL Next]** de delegatie te verwijderen.

## Foutcodes {#FAQ}

In deze sectie worden de foutberichten weergegeven die kunnen optreden wanneer u probeert de delegatie van een subdomein te verwijderen:

| Foutcode | Bericht | Beschrijving |
|  ---  |  ---  |  ---  |
| 8002 | Gevraagde verwijdering van gedelegeerd domein kan niet worden behandeld omdat er een soortgelijk overlappend verzoek in behandeling is. Probeer het over 3 dagen | Er wordt al een subdomeindelegatie verwijderd voor de geselecteerde instantie. Wacht tot 3 dagen om een nieuwe verwijdertaak te starten. |
| 8003 | Gevraagde verwijdering van gedelegeerd domein wordt niet ondersteund voor deze instantie. | Het verwijderen van delegatie wordt niet ondersteund voor het geselecteerde subdomein vanwege een technisch probleem. Neem contact op met de klantenservice. |
| 8004 | Gevraagde verwijdering van gedelegeerd domein is niet toegestaan omdat er in dit geval slechts één domein is. | Er is slechts één subdomein gedelegeerd voor de geselecteerde instantie. Verwijdering van delegatie is niet toegestaan. |
| 8005 | Gevraagde verwijdering van gedelegeerd domein wordt niet ondersteund voor deze configuratie. | Het verwijderen van delegatie wordt niet ondersteund voor het geselecteerde subdomein vanwege een technisch probleem. Neem contact op met de klantenservice. |
| 8006 | Gevraagde verwijdering van gedelegeerd domein is om onbekende redenen niet toegestaan. Neem contact op met de klantenservice. | Het verwijderen van delegaties wordt niet ondersteund voor de geselecteerde instantie vanwege een onbekend probleem. Neem contact op met de klantenservice. |
