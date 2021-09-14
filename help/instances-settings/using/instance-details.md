---
product: campaign
solution: Campaign
title: Instantiedetails
description: Leer hoe u de instantiedetails in het Configuratiescherm kunt bewaken
feature: Control Panel
role: Architect
level: Experienced
exl-id: 02819bfc-9886-43fc-8014-9bfe64c42048
source-git-commit: 599cb22da734f53c0b06583be3e47668dcb57ef1
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 84%

---

# Instantiedetails {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="Informatie over Instantiedetails"
>abstract="Bekijk de details van uw Adobe Campaign-instanties: types, namen, buildinformatie en mogelijke upgradeaanbevelingen."
>additional-url="https://https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/latest-release.html" text="Opmerkingen bij de release van Campaign Classic"
>additional-url="https://https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/release-notes.html" text="Opmerkingen bij de release van Campaign Standard"

## Informatie over Instantiedetails {#about-instance-details}

>[!IMPORTANT]
>
>Deze functie is alleen beschikbaar voor Campaign Classic v7- en Campagne v8-instanties.

Uw Adobe Campaign-instantiearchitectuur kan verschillende servers bevatten om de flexibiliteit van marketingactiviteiten mogelijk te maken. U kunt bijvoorbeeld marketing-, realtime- (of Message Center-) en mid-sourcing-servers hebben ter ondersteuning van uw instantie.

Met de functie Instantiedetails kunt u de platte architectuur van uw instantie weergeven. Naast serverinformatie wordt u ook geïnformeerd of uw instantie up-to-date is en worden waar nodig upgrades aanbevolen.

>[!NOTE]
>
>We raden u aan om uw instanties ten minste één keer per jaar te upgraden om te voorkomen dat de prestaties afnemen en om te profiteren van de nieuwste functies en oplossingen die Adobe Campaign Classic te bieden heeft.

**Verwante onderwerpen:**

* [Een build-upgrade uitvoeren](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Adobe Campaign bijwerken](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Informatie over uw instanties ophalen {#retrieving-information-about-instances}

Voer de volgende stappen uit om informatie op te halen over de servers die zijn verbonden met uw instanties:

1. Open de **[!UICONTROL Instances Settings]**-kaart om toegang te krijgen tot het tabblad **[!UICONTROL Instance Details]**.

   >[!NOTE]
   >
   >Als de Instellingenkaart van de Instantie niet zichtbaar is op de homepage van het Controlebord, betekent dit dat uw IMS Organisatie ID niet met om het even welke instanties van Adobe Campaign Classic wordt geassocieerd

1. Selecteer in het linkerdeelvenster de gewenste instantie Campagne.

   >[!NOTE]
   >
   >Alle Campaign-instanties worden weergegeven in de lijst in het linkerdeelvenster. Aangezien de functie Instance Details specifiek is voor Campaign Classic-instanties, wordt het bericht ‘Non-Applicable Instance’ weergegeven als u een Campaign Standard-instantie selecteert.

1. U ziet de servers die met de instantie verbonden zijn.

   ![](assets/instance_details.png)

Beschikbare informatie is:

* **[!UICONTROL Type]**: Het type server. Mogelijke waarden zijn MKT (Marketing), MID (Mid-sourcing) en RT (Message Center/Real-time messaging).
* **[!UICONTROL Name]**: de naam van de server.
* **[!UICONTROL Build:]** de buildversie die op de server is geïnstalleerd.
* **[!UICONTROL Upgrade info]**: deze kolom geeft aan of er een update voor de server vereist is.
   * Groen: De server is up-to-date. Er is geen upgrade vereist.
   * Geel: U doet er goed aan een upgrade uit te voeren. De nieuwste functies en oplossingen ontbreken.
   * Rood: Voer zo snel mogelijk een upgrade uit. Er ontbreken nieuwe functies en de prestaties van de server zijn mogelijk niet optimaal.

Als een van uw servers moet worden bijgewerkt, raadpleegt u [deze documentatie](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) voor meer informatie over verdere stappen.

## Algemene vragen {#common-questions}

**Ik zie de MID-server niet in mijn instantiearchitectuur. Betekent dit dat mijn instanties niet correct werken? Heb ik de RT-instantie nodig voor iets wat ik vandaag niet kan doen?**

Uw eigen instantie kan er heel anders uitzien en heeft mogelijk niet alle typen servers of heeft meerdere servers van hetzelfde type. Als u een bepaald type server niet hebt, betekent dit niet dat u geen realtimebericht kunt verzenden of andere soorten activiteiten kunt uitvoeren. U kunt aanvullende servercapaciteit aanvragen. Hiervoor worden extra kosten in rekening gebracht.

Neem contact op met de klantenservice als u denkt dat bepaalde servers niet worden weergegeven op de pagina Instance Details. Noteer de specifieke instantie-URL in uw bericht.
