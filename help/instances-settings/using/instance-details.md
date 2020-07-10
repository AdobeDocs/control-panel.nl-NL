---
title: Instantiedetails
description: Leer hoe u de instantiedetails in het Configuratiescherm kunt controleren
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Instantiedetails {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="Informatie over Instantie"
>abstract="Bekijk de details van je Adobe Campaign-instanties: types, namen, bouwt informatie en mogelijke verbeteringsaanbevelingen."
>additional-url="https://docs.adobe.com/content/help/en/campaign-classic/using/release-notes/latest-release.html" text="Opmerkingen bij de release van Campaign Classic"
>additional-url="https://docs.adobe.com/content/help/en/campaign-standard/using/release-notes/release-notes.html" text="Opmerkingen bij de release van Campaign Standard"

>[!IMPORTANT]
>
>Deze functie is alleen beschikbaar voor Campaign Classic-instanties.

## Informatie over instanties {#about-instance-details}

Uw Adobe Campaign Classic-instantiearchitectuur kan verschillende servers bevatten om de flexibiliteit van marketingactiviteiten mogelijk te maken. Bijvoorbeeld, kunt u Marketing hebben, Echte tijd (of het Centrum van het Bericht) en Midden het Bronnen servers die uw instantie steunen.

Met de functie Instantie details kunt u de platte architectuur van uw instantie weergeven. Naast serverinformatie, laat het u ook weten of uw instantie huidig is of niet, evenals adviseert verbeteringen wanneer nodig.

>[!NOTE]
>
>We raden u aan om uw instanties ten minste één keer per jaar te upgraden om te voorkomen dat de prestaties afnemen en om te profiteren van de nieuwste functies en oplossingen die Adobe Campaign Classic te bieden heeft.

**Verwante onderwerpen:**

* [Een build-upgrade uitvoeren](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Adobe Campaign bijwerken](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Informatie over uw instanties ophalen {#retrieving-information-about-instances}

Voer de volgende stappen uit om informatie op te halen over de servers die zijn aangesloten op uw instanties:

1. Open de **[!UICONTROL Instances Settings]**-kaart om toegang te krijgen tot het tabblad **[!UICONTROL Instance Details]**.

   >[!NOTE]
   >
   >Als de Instellingenkaart van de Instantie niet zichtbaar is op de homepage van het Controlebord, betekent dit dat uw IMS Organisatie ID niet met om het even welke Classic Instanties van Adobe Campaign wordt geassocieerd

1. Selecteer in het linkerdeelvenster het gewenste Campaign Classic-exemplaar.

   >[!NOTE]
   >
   >Alle instanties van Campagne worden weergegeven in de lijst in het linkerdeelvenster. Aangezien de functie Instantiedetails alleen is toegewezen aan Campaign Classic-instanties, wordt het bericht &quot;Niet-toepasbare instantie&quot; weergegeven als u een Campaign Standard-instantie selecteert.

1. De servers die met de instantiesvertoning worden verbonden.

   ![](assets/instance_details.png)

Beschikbare informatie is:

* **[!UICONTROL Type]**: het type van de server. Mogelijke waarden zijn MKT (Marketing), MID (Midden-sourcing) en RT (Message Center / Real-time messaging).
* **[!UICONTROL Name]**: de naam van de server.
* **[!UICONTROL Build:]** de buildversie die op de server is geïnstalleerd.
* **[!UICONTROL Upgrade info]**: Deze kolom geeft aan of er een update voor de server is vereist.
   * Groen: als de server actief is, is geen upgrade vereist.
   * Geel: U kunt een upgrade uitvoeren. De nieuwste functies en oplossingen ontbreken.
   * Rood: zo snel mogelijk een upgrade uitvoeren. Er ontbreken nieuwe functies en de prestaties van de server zijn mogelijk niet optimaal.

Als een van uw servers moet worden bijgewerkt, raadpleegt u [deze documentatie](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) voor meer informatie over hoe u verder kunt gaan.

## Algemene vragen {#common-questions}

**Ik zie de MID-server niet op mijn instantiearchitectuur. Betekent dit dat mijn instanties niet correct werken? Heb ik de RT-instantie nodig voor iets wat ik vandaag niet kan doen?**

Uw eigen instantie kan er heel anders uitzien en heeft mogelijk niet alle typen servers, of meerdere servers van dezelfde server. Als u niet één type server of een ander type server hebt, betekent dit niet dat u geen real-time bericht kunt verzenden of andere soorten activiteiten kunt uitvoeren. U kunt aanvullende servercapaciteit aanvragen. Er worden extra kosten in rekening gebracht.

Neem contact op met de klantenservice als u denkt dat bepaalde servers niet worden weergegeven op de pagina &quot;Instantiedetails&quot;. Let op de specifieke instantie-URL in uw bericht.
