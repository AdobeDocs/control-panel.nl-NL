---
title: IP-aanbieding toestaan
description: Leer hoe te om IP adressen aan de lijst van gewenste personen in het Controlebord voor instantietoegang toe te voegen
translation-type: tm+mt
source-git-commit: abe22509e3389874e0b3586a99a1ad2d49681ed8
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---


# IP-aanbieding toestaan {#ip-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="Aanbieding via IP toestaan"
>abstract="Voeg IP adressen aan de lijst van gewenste personen toe om tot uw instanties toegang te hebben."
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="Video over demo bekijken"

>[!IMPORTANT]
>
>Deze functie is alleen beschikbaar voor Campaign Classic-instanties.

## Aanbieding via IP toestaan {#about-ip-allow-listing}

Standaard is uw Adobe Campaign Classic-instantie niet toegankelijk via verschillende IP-adressen.

Als uw IP adres niet aan de lijst van gewenste personen is toegevoegd, zult u niet aan login aan de instantie van dit adres kunnen. Op dezelfde manier, kunt u geen API met uw Centrum van het Bericht of instantie van de Marketing kunnen verbinden als het IP adres niet uitdrukkelijk aan de lijst van gewenste personen met de instantie is toegevoegd.

Met het Configuratiescherm kunt u nieuwe verbindingen met uw instanties instellen door IP-adresbereiken aan de lijst van gewenste personen toe te voegen. Volg de onderstaande stappen om dit te doen.

Zodra IP de adressen op de lijst van gewenste personen zijn, kunt u de exploitanten van de Campagne tot stand brengen en verbinden aan hen zodat de gebruikers tot de instantie kunnen toegang hebben.

## Aanbevolen procedures {#best-practices}

Volg de onderstaande aanbevelingen en beperkingen wanneer u IP-adressen toevoegt aan de lijst van gewenste personen in het Configuratiescherm.

* **Laat IP geen toegang tot alle Types** van Toegang toe als u niet het IP adres om met uw servers van RT, of de veiligheidsstreek van AEM van plan bent te verbinden.
* **Als u tijdelijk toegang tot uw instantie voor een IP adres** toeliet, zorg ervoor om de IP adressen uit de lijst van gewenste personen te verwijderen zodra u het niet meer nodig hebt om met uw instantie te verbinden.
* **Wij adviseren niet IP adressen van openbare plaatsen aan de lijst van gewenste personen** (luchthavens, hotels, enz.) toe te voegen. Gelieve te gebruiken uw adres van bedrijfsVPN om uw instantie te allen tijde veilig te houden.

## IP-adressen toevoegen aan de lijst van gewenste personen voor Instance Access {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="Nieuw IP-bereik toevoegen"
>abstract="Bepaal de IP waaier die u aan de lijst van gewenste personen wilt toevoegen om met uw instantie te verbinden."

Ga als volgt te werk om IP-adressen aan de lijst van gewenste personen toe te voegen:

1. Open the **[!UICONTROL Instances Settings card]** to access the IP allow listing tab, then click **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Als de Instellingenkaart van de Instantie niet zichtbaar is op de homepage van het Controlebord, betekent dit dat uw identiteitskaart IMS ORG niet met om het even welke Klassieke Instanties van Adobe Campaign wordt geassocieerd

   ![](assets/ip_whitelist_list1.png)

1. Vul de informatie voor de IP Waaier in die u aan de lijst van gewenste personen wilt toevoegen zoals hieronder beschreven.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**: De instanties waaraan de IP adressen zullen kunnen verbinden. Verschillende instanties kunnen tegelijkertijd worden gemanipuleerd. IP staat bijvoorbeeld toe dat een lijst op zowel Productie- als Stage-instanties kan worden uitgevoerd via dezelfde stap.
   * **[!UICONTROL IP Range]**: De IP waaier die u aan de lijst van gewenste personen, in het formaat wilt toevoegen CIDR. Merk op dat een IP waaier geen bestaande waaier op de lijst van gewenste personen kan overlappen. In dat geval, schrap eerst de waaier die overlappende IP bevat.
   >[!NOTE]
   >
   >CIDR (het Klasseloze Verpletteren inter-Domein) is het gesteunde formaat wanneer het toevoegen van IP waaiers met de interface van het Controlebord. De syntaxis bestaat uit een IP-adres, gevolgd door een &#39;/&#39;-teken en een decimaal getal. De opmaak en syntaxis worden volledig in [dit artikel](https://whatismyipaddress.com/cidr)beschreven.
   >
   >U kunt op internet zoeken naar gratis onlinegereedschappen waarmee u het IP-bereik dat u hebt, kunt omzetten in de CIDR-indeling.

   * **[!UICONTROL Label]**: Het label dat in de lijst van gewenste personen wordt weergegeven.
   * **[!UICONTROL Name]**: De naam moet uniek zijn voor het toegangstype, de instantie (in het geval van een externe API-verbinding) en het IP-adres.


1. Specificeer het type van toegang dat u aan de IP adressen wilt verlenen:

   * **[!UICONTROL Campaign Console Access]**: De IP-adressen mogen verbinding maken met de Campaign Classic-console. De toegang van de Console wordt toegelaten voor slechts instanties van de Marketing. Toegang tot MID- en RT-instanties is niet toegestaan en daarom niet ingeschakeld.
   * **[!UICONTROL AEM connection]**: De opgegeven AEM IP-adressen mogen verbinding maken met de marketinginstantie.
   * **[!UICONTROL External API connection]**: Externe API&#39;s met de opgegeven IP-adressen kunnen verbinding maken met de instantie Marketing en/of Message Center (RT). Merk op dat de verbinding aan de console van instanties RT niet wordt toegelaten.
   ![](assets/ip_whitelist_acesstype.png)

1. Klik op de **[!UICONTROL Save]** knop. De IP Waaier wordt toegevoegd aan de lijst van gewenste personen.

   ![](assets/ip_whitelist_added.png)

Om IP waaiers van de lijst van gewenste personen te schrappen, selecteer hen dan de **[!UICONTROL Delete IP range]** knoop.

**Verwante onderwerpen:**
* [IP staat lijst (zelfstudie video) toe](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-allow-listing.html)
* [Een beveiligingszone koppelen aan een operator](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
