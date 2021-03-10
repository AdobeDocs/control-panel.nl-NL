---
product: campaign
solution: Campaign
title: IP-bereiken toevoegen aan de lijst van gewenste IP-adressen
description: Leer hoe u IP-bereiken toevoegt aan de lijst van gewenste IP-adressen voor toegang tot SFTP-servers
feature: 'Configuratiescherm '
role: Architect
level: Ervaren
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 94%

---


# IP-bereiken toevoegen aan de lijst van gewenste IP-adressen {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="IP-adressen toevoegen aan de lijst van gewenste IP-adressen"
>abstract="Op dit tabblad kunt u IP-bereiken toevoegen aan de lijst van gewenste IP-adressen om een verbinding met uw SFTP-servers tot stand te brengen. Alleen SFTP-servers waartoe u toegang hebt, worden hier weergegeven. Neem contact op met uw beheerder om toegang tot andere SFTP-servers aan te vragen."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Demovideo bekijken"

SFTP-servers zijn beveiligd. Als u er toegang toe wilt krijgen om bestanden te bekijken of nieuwe bestanden te schrijven, moet u het openbare IP-adres van het systeem dat of de client die gebruikmaakt van de servers, toevoegen aan de lijst van gewenste IP-adressen.

![](assets/do-not-localize/how-to-video.png) Deze functie in video ontdekken met  [Campagne ](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=en#sftp-management) Classicor  [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=en#sftp-management)

## Informatie over de CIDR-indeling {#about-cidr-format}

CIDR (Classless Inter-Domain Routing) is de ondersteunde indeling bij het toevoegen van IP-bereiken met de interface van het Configuratiescherm.

De syntaxis bestaat uit een IP-adres, gevolgd door een slash (/) en een decimaal getal. De indeling en bijbehorende syntaxis worden uitgebreid beschreven in [dit artikel](https://whatismyipaddress.com/cidr).

U kunt op internet zoeken naar gratis online tools waarmee u het IP-bereik dat u hebt, kunt omzetten in CIDR-indeling.

## Aanbevolen procedures {#best-practices}

Volg de onderstaande aanbevelingen en beperkingen wanneer u IP-adressen toevoegt aan de lijst van gewenste IP-adressen in het Configuratiescherm.

* **Voeg IP-bereiken aan de lijst van gewenste IP-adressen toe**, niet afzonderlijke IP-adressen. Als u één IP-adres aan de lijst van gewenste IP-adressen wilt toevoegen, voegt u er ‘/32’ aan toe om aan te geven dat het bereik slechts één IP-adres bevat.
* **Voeg geen zeer grote bereiken, bijvoorbeeld met meer dan 265 IP-adressen, aan de lijst van gewenste IP-adressen toe**. Alle bereiken in CIDR-indeling, die tussen /0 en /23 liggen, worden door het Configuratiescherm verworpen.
* Alleen **openbare IP-adressen** kunnen aan de lijst van gewenste IP-adressen worden toegevoegd.
* **Verwijder regelmatig IP-adressen** die u niet meer nodig hebt uit de lijst van gewenste IP-adressen.

## IP-adressen toevoegen aan de lijst van gewenste IP-adressen {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Nieuw IP-bereik toevoegen"
>abstract="Definieer de IP-bereiken die u aan de lijst van gewenste IP-adressen wilt toevoegen om verbinding te maken met uw SFTP-servers."

Ga als volgt te werk om een IP-bereik aan de lijst van gewenste IP-adressen toe te voegen:

1. Open de **[!UICONTROL SFTP]**-kaart en selecteer vervolgens het tabblad **[!UICONTROL IP Allow Listing]**.
1. De lijst met IP-adressen in de lijst van gewenste IP-adressen wordt voor elke instantie weergegeven. Selecteer de gewenste instantie in de lijst aan de linkerkant en klik op de knop **[!UICONTROL Add new IP range]**.

   ![](assets/control_panel_add_range.png)

1. Definieer het IP-bereik dat u aan de lijst van gewenste IP-adressen wilt toevoegen, in de indeling CIDR, en definieer vervolgens het label dat in de lijst wordt weergegeven.

   >[!NOTE]
   >
   >Deze speciale tekens zijn toegestaan in het veld Label:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >Een IP-bereik mag een bestaand bereik in de lijst van gewenste IP-adressen niet overlappen. Verwijder in dat geval eerst het bereik met de overlappende IP-adressen.
   >
   >Het is mogelijk om een bereik toe te voegen aan de lijst van gewenste IP-adressen voor meerdere instanties. U doet dit door op de pijltoets omlaag te drukken of de eerste letters van de gewenste instantie te typen en deze vervolgens te selecteren in de lijst met suggesties.

   ![](assets/control_panel_add_range3.png)

1. Klik op de knop **[!UICONTROL Save]**. De toevoeging van een IP-bereik aan de lijst van gewenste IP-adressen wordt als PENDING weergegeven tot het verzoek volledig is verwerkt. Dit duurt meestal slechts een paar seconden.

Als u IP-bereiken uit de lijst van gewenste IP-adressen wilt verwijderen, selecteert u deze en klikt u op de knop **[!UICONTROL Delete IP range]**.

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Het is momenteel niet mogelijk om een bereik in de lijst van gewenste IP-adressen te bewerken. Als u een IP-bereik wilt wijzigen, verwijdert u het en maakt u een nieuw bereik dat aan uw behoeften beantwoordt.

## Wijzigingen bijhouden {#monitoring-changes}

Met **[!UICONTROL Job Logs]** op de startpagina van het Configuratiescherm kunt u alle wijzigingen bijhouden die zijn aangebracht in IP-adressen in de lijst van gewenste IP-adressen.

Raadpleeg [deze sectie](../../discover/using/discovering-the-interface.md) voor meer informatie over de interface van het Configuratiescherm.

![](assets/control_panel_ip_log.png)
