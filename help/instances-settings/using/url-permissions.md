---
title: URL-machtigingen
description: Leer hoe u URL-machtigingen beheert in het Configuratiescherm
translation-type: tm+mt
source-git-commit: 3faeb9651681a9edd18cf889fff65b02644cb690
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---


# URL-machtigingen {#url-permissions}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_urlpermissions"
>title="Informatie over URL-machtigingen"
>abstract="Beheer de URL&#39;s waarmee uw Adobe Campaign-instanties verbinding kunnen maken."
>additional-url="https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4" text="Video over demo bekijken"

>[!IMPORTANT]
>
>Deze functie is alleen beschikbaar voor Campaign Classic-instanties, vanaf build 8850. Als u een vorige build gebruikt, moet u een upgrade uitvoeren om deze functie te gebruiken.

## Informatie over URL-machtigingen {#about-url-permissions}

De standaardlijst met URL&#39;s die door JavaScript-codes kunnen worden aangeroepen (workflows, enz.) door uw Campaign Classic-instanties beperkt zijn. Dit zijn URL&#39;s waarmee uw instanties correct kunnen werken.

Instanties mogen standaard geen verbinding maken met externe URL&#39;s. In het Configuratiescherm kunt u enkele externe URL&#39;s toevoegen aan de lijst met geoorloofde URL&#39;s, zodat uw instantie er verbinding mee kan maken. Hierdoor kunt u uw Campagne-instanties verbinden met externe systemen, zoals bijvoorbeeld SFTP-servers of websites, om de overdracht van bestanden en/of gegevens mogelijk te maken.

Wanneer een URL is toegevoegd, wordt hiernaar verwezen in het configuratiebestand van de instantie (serverConf.xml).

**Verwante onderwerpen:**

* [Campagneserver configureren](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html)
* [Uitgaande verbindingsbeveiliging](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Outgoing_connection_protection)
* [URL-machtigingen toevoegen (videozelfstudie)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/adding-url-permissions.html)

## Aanbevolen procedures {#best-practices}

* Sluit de Campagne-instantie niet aan op websites/servers waarmee u geen verbinding wilt maken.
* Verwijder URL&#39;s waarmee u niet meer werkt. Houd er echter rekening mee dat als een ander gedeelte van uw bedrijf nog steeds verbinding maakt met de URL die u hebt verwijderd, niemand deze opnieuw kan gebruiken.
* Het regelpaneel ondersteunt **http**-, **https**- en **sftp** -protocollen. Het invoeren van ongeldige URL&#39;s of protocollen leidt tot fouten.

## URL-machtigingen beheren {#managing-url-permissions}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_url_add"
>title="Nieuwe URL toevoegen"
>abstract="Voeg URLs toe om verbindingen aan uw instantie van de Campagne toe toe te staan."

Ga als volgt te werk om een URL toe te voegen waarmee uw instantie verbinding kan maken:

1. Open de **[!UICONTROL Instances Settings]**-kaart om toegang te krijgen tot het tabblad **[!UICONTROL URL Permissions]**.

   >[!NOTE]
   >
   >Als de Instellingenkaart van de Instantie niet zichtbaar is op de homepage van het Controlebord, betekent dit dat uw identiteitskaart IMS ORG niet met om het even welke Klassieke Instanties van Adobe Campaign wordt geassocieerd
   >
   >Het tabblad <b><span class="uicontrol">URL-machtigingen</span></b> bevat alle externe URL&#39;s waarmee uw instantie verbinding kan maken. Deze lijst bevat geen URL&#39;s die vereist zijn om de campagne te laten werken (bijvoorbeeld verbindingen tussen infrastructuuronderdelen).

1. Selecteer in het linkerdeelvenster het gewenste exemplaar en klik op de **[!UICONTROL Add new URL]** knop.

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >Alle instanties van Campagne worden weergegeven in de lijst in het linkerdeelvenster.
   >
   >Aangezien het beheer van URL-machtigingen alleen aan Campaign Classic-instanties is toegewezen, wordt het bericht &quot;Niet-toepasselijke instantie&quot; weergegeven als u een Campaign Standard-instantie selecteert.

1. Typ de URL die u wilt autoriseren met het bijbehorende protocol (http, https of sftp).

   >[!NOTE]
   >
   >Het is mogelijk meerdere instanties te autoriseren om verbinding te maken met de URL. U doet dit door ze rechtstreeks vanuit het veld Instantie(s) toe te voegen door de eerste letter te typen.

   ![](assets/add_url2.png)

1. De URL wordt toegevoegd aan de lijst en u kunt er nu verbinding mee maken.

   >[!NOTE]
   >
   >De &quot;/.*&quot;-tekens worden automatisch toegevoegd aan het einde van de URL die u invoert nadat deze is gevalideerd, zodat deze alle subpagina&#39;s van de ingevoerde pagina beslaan.

   ![](assets/add_url_listnew.png)

U kunt een URL op elk gewenst moment verwijderen door deze te selecteren en op de **[!UICONTROL Delete URL]** knop te klikken.

Houd er rekening mee dat als u een URL verwijdert, uw instantie deze niet opnieuw kan aanroepen.

## Algemene vragen {#common-questions}

**Ik heb een nieuwe URL toegevoegd, maar mijn instantie kan nog steeds geen verbinding maken met die URL. Waarom is dat?**

In sommige gevallen moeten URL&#39;s waarmee u verbinding probeert te maken een vermelding, wachtwoord of een andere vorm van verificatie toestaan. Aanvullende verificatie wordt niet beheerd in het Configuratiescherm.
