---
title: Witelende IP-reeks
description: Leer hoe te whitelist IP waaiers voor de servers van SFTP toegang hebben
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 1%

---


# Witelende IP-reeks {#ip-range-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Informatie over IP-whitelisting"
>abstract="Op dit tabblad kunt u een whitelist-IP-bereik opgeven om een verbinding tot stand te brengen met uw SFTP-servers. Alleen SFTP-servers waartoe u toegang hebt, worden hier weergegeven. Neem contact op met uw beheerder om toegang tot andere SFTP-servers aan te vragen."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Video over demo bekijken"

SFTP-servers zijn beveiligd. Om tot hen te kunnen toegang hebben om dossiers te bekijken of nieuwe degenen te schrijven, moet u het openbare IP adres van het systeem of de cliënt whitelist die tot de servers toegang heeft.

## Informatie over de CIDR-indeling {#about-cidr-format}

CIDR (het Klasseloze Verpletteren inter-Domein) is het gesteunde formaat wanneer het toevoegen van IP waaiers met de interface van het Controlebord.

De syntaxis bestaat uit een IP-adres, gevolgd door een &#39;/&#39;-teken en een decimaal getal. De opmaak en syntaxis worden volledig in [dit artikel](https://whatismyipaddress.com/cidr)beschreven.

U kunt op internet zoeken naar gratis onlinegereedschappen waarmee u het IP-bereik dat u hebt, kunt omzetten in de CIDR-indeling.

## Aanbevolen procedures {#best-practices}

Volg de onderstaande aanbevelingen en beperkingen wanneer u een zwevend IP-adres opgeeft in het Configuratiescherm.

* **IP van whitelist waaiers** eerder dan enige IP adressen. Aan whitelist één enkel IP adres, voeg &#39;/32&#39; aan het toe om erop te wijzen dat de waaier slechts één enkel IP omvat.
* **Witte randen** niet erg breed, bijvoorbeeld met > 265 IP-adressen. Het Controlebord zal om het even welke CIDR-formaat waaiers verwerpen die tussen /0 en /23 zijn.
* Slechts kunnen de **openbare IP adressen** worden gewhitelisteerd.
* Zorg ervoor om **regelmatig gewhitelisteerde IP adressen** te schrappen die u niet meer nodig hebt.

## Whitelisting IP-adressen {#whitelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Nieuw IP-bereik toevoegen"
>abstract="Definieer de IP-bereiken die u als whitelist wilt gebruiken om verbinding te maken met uw SFTP-servers."

Aan whitelist een IP waaier, volg deze stappen:

1. Open de **[!UICONTROL SFTP]**-kaart en selecteer vervolgens het tabblad **[!UICONTROL IP Whistelisting]**.
1. De lijst van whitelisted IP adressen toont voor elke instantie. Selecteer de gewenste instantie in de lijst aan de linkerkant en klik op de **[!UICONTROL Add new IP range]** knop.

   ![](assets/control_panel_add_range.png)

1. Bepaal de IP Waaier die u, in het formaat wilt whitelist CIDR, dan het etiket bepalen dat in de lijst zal tonen.

   >[!NOTE]
   >
   >Deze speciale tekens zijn toegestaan in het veld Label:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >Een IP-bereik kan een bestaande whitelisted-reeks niet overlappen. In dat geval, schrap eerst de waaier die overlappende IP bevat.
   >
   >Het is mogelijk om een bereik voor meerdere instanties witter te maken. U doet dit door op de pijltoets omlaag te drukken of de eerste letters van de gewenste instantie te typen en deze vervolgens te selecteren in de lijst met suggesties.

   ![](assets/control_panel_add_range3.png)

1. Klik op de **[!UICONTROL Save]** knop. IP de toevoeging van whitelist zal als IN BEHANDELING worden getoond tot het verzoek volledig wordt verwerkt. Dit zou slechts een paar seconden moeten duren.

Om gewhitelisteerde IP waaiers te schrappen, selecteer hen dan de **[!UICONTROL Delete IP range]** knoop.

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Het is momenteel niet mogelijk om een whitelisted-bereik te bewerken. Om een IP waaier te wijzigen, schrap het, dan creeer één die aan uw behoeften beantwoordt.

## Wijzigingen bijhouden {#monitoring-changes}

Met **[!UICONTROL Job Logs]** de startpagina van het Configuratiescherm kunt u alle wijzigingen controleren die zijn aangebracht in een zwevend IP-adres.

Raadpleeg [deze sectie](../../discover/using/discovering-the-interface.md)voor meer informatie over de interface van het Configuratiescherm.

![](assets/control_panel_ip_log.png)
