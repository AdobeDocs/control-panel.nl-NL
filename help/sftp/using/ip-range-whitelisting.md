---
title: Aanbieding in IP-bereik toegestaan
description: Leer hoe te om IP waaiers aan toe te voegen staan lijst voor de servertoegang van SFTP
translation-type: tm+mt
source-git-commit: 3faeb9651681a9edd18cf889fff65b02644cb690
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 1%

---


# Aanbieding in IP-bereik toegestaan {#ip-range-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Aanbieding via IP toestaan"
>abstract="Op dit tabblad kunt u IP-bereiken toevoegen aan de lijst met toegestane bereiken om een verbinding met uw SFTP-servers tot stand te brengen. Alleen SFTP-servers waartoe u toegang hebt, worden hier weergegeven. Neem contact op met uw beheerder om toegang tot andere SFTP-servers aan te vragen."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Video over demo bekijken"

SFTP-servers zijn beveiligd. Om tot hen te kunnen toegang hebben om dossiers te bekijken of nieuwe te schrijven, moet u het openbare IP adres van het systeem of de cliënt toevoegen die tot de servers aan toestaan lijst toegang heeft.

## Informatie over de CIDR-indeling {#about-cidr-format}

CIDR (het Klasseloze Verpletteren inter-Domein) is het gesteunde formaat wanneer het toevoegen van IP waaiers met de interface van het Controlebord.

De syntaxis bestaat uit een IP-adres, gevolgd door een &#39;/&#39;-teken en een decimaal getal. De opmaak en syntaxis worden volledig in [dit artikel](https://whatismyipaddress.com/cidr)beschreven.

U kunt op internet zoeken naar gratis onlinegereedschappen waarmee u het IP-bereik dat u in handen hebt, kunt omzetten in de CIDR-indeling.

## Aanbevolen procedures {#best-practices}

Volg de onderstaande aanbevelingen en beperkingen wanneer u IP-adressen toevoegt aan de lijst Toestaan in het Configuratiescherm.

* **Voeg IP waaiers aan toe toestaan lijst** eerder dan enige IP adressen. Om één enkel IP adres aan toe te voegen staat lijst toe, voeg &#39;/32&#39; aan het toe om erop te wijzen dat de waaier slechts één enkel IP omvat.
* **Voeg geen zeer brede waaiers aan de toegestane lijst**, bijvoorbeeld met inbegrip van > 265 IP adressen toe. Het Controlebord zal om het even welke CIDR-formaat waaiers verwerpen die tussen /0 en /23 zijn.
* Alleen **openbare IP-adressen** kunnen aan de lijst met toegestane adressen worden toegevoegd.
* Zorg ervoor om IP adressen **** regelmatig te schrappen die u niet meer van toestaat lijst nodig hebt.

## IP-adressen toevoegen aan de lijst Allow {#whitelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Nieuw IP-bereik toevoegen"
>abstract="Definieer de IP-bereiken die u aan de lijst Allow wilt toevoegen om verbinding te maken met uw SFTP-servers."

Ga als volgt te werk om een IP-bereik toe te voegen aan de lijst Allow:

1. Open de **[!UICONTROL SFTP]**-kaart en selecteer vervolgens het tabblad **[!UICONTROL IP Whistelisting]**.
1. De lijst met IP-adressen in de lijst Toestaan wordt voor elke instantie weergegeven. Selecteer de gewenste instantie in de lijst aan de linkerkant en klik op de **[!UICONTROL Add new IP range]** knop.

   ![](assets/control_panel_add_range.png)

1. Bepaal de IP Waaier die u aan toestaan lijst, in het formaat wilt toevoegen CIDR, dan het etiket bepalen dat in de lijst zal tonen.

   >[!NOTE]
   >
   >Deze speciale tekens zijn toegestaan in het veld Label:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >Een IP-bereik kan een bestaand bereik op de lijst met toegestane waarden niet overlappen. In dat geval, schrap eerst de waaier die overlappende IP bevat.
   >
   >Het is mogelijk om een bereik in de lijst voor meerdere instanties toestaan toe te voegen. U doet dit door op de pijltoets omlaag te drukken of de eerste letters van de gewenste instantie te typen en deze vervolgens te selecteren in de lijst met suggesties.

   ![](assets/control_panel_add_range3.png)

1. Klik op de **[!UICONTROL Save]** knop. IP de toevoeging aan toestaan lijst zal als IN BEHANDELING worden getoond tot het verzoek volledig wordt verwerkt. Dit zou slechts een paar seconden moeten duren.

Om IP waaiers van de allow lijst te schrappen, selecteer hen dan de **[!UICONTROL Delete IP range]** knoop.

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Het is momenteel niet mogelijk om een bereik in de lijst voor toestaan te bewerken. Om een IP waaier te wijzigen, schrap het, dan creeer één die aan uw behoeften beantwoordt.

## Wijzigingen bijhouden {#monitoring-changes}

Met **[!UICONTROL Job Logs]** de startpagina van het Configuratiescherm kunt u alle wijzigingen controleren die zijn aangebracht in IP-adressen in de lijst met toegestane adressen.

Raadpleeg [deze sectie](../../discover/using/discovering-the-interface.md)voor meer informatie over de interface van het Configuratiescherm.

![](assets/control_panel_ip_log.png)