---
product: campaign
solution: Campaign
title: Aanmelden bij uw SFTP-server
description: Leer hoe u zich aanmeldt bij uw SFTP-server
feature: Control Panel
role: Architect
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# Aanmelden bij uw SFTP-server {#logging-into-sft-server}

In de onderstaande stappen wordt beschreven hoe u verbinding kunt maken met uw SFTP-server via uw SFTP-clienttoepassing.

![](assets/do-not-localize/how-to-video.png)[ Ontdek deze functie in video](https://video.tv.adobe.com/v/27263?quality=12)

Voordat u zich aanmeldt bij de server, moet u controleren of:

* Uw SFTP-server is **gehost door Adobe**.
* Uw **gebruikersnaam** is ingesteld voor de server. U kunt deze informatie rechtstreeks controleren in het Configuratiescherm, in het dialoogvenster **Sleutelbeheer** van de SFTP-kaart.
* U hebt een **persoonlijke en openbare sleutel** om u aan te melden bij de SFTP-server. Zie [deze sectie](../../sftp/using/key-management.md) voor meer informatie over het toevoegen van de SSH-toets.
* Uw **het openbare IP adres is toegevoegd aan de lijst van gewenste personen** op de SFTP-server. Indien niet, raadpleeg [deze sectie](../../sftp/using/ip-range-allow-listing.md) voor meer op hoe te om uw IP waaier aan de lijst van gewenste personen toe te voegen.
* U hebt toegang tot een **SFTP-clientsoftware**. U kunt uw afdeling van IT voor de cliënttoepassing raadplegen SFTP die zij om adviseren te gebruiken, of onderzoek naar op Internet als dit door uw bedrijfsbeleid wordt toegestaan.

Voer de volgende stappen uit om verbinding te maken met uw SFTP-server:

1. Start het Configuratiescherm en selecteer vervolgens het **[!UICONTROL Key Management]** van de **[!UICONTROL SFTP]** kaart.

   ![](assets/sftp_card.png)

1. Start de SFTP-clienttoepassing en kopieer en plak het serveradres vanuit het Configuratiescherm, gevolgd door &quot;campagne.adobe.com&quot;. Vul vervolgens uw gebruikersnaam in.

   ![](assets/do-not-localize/connect1.png)

1. In de **[!UICONTROL SSH Private Key]** selecteert u het bestand met de persoonlijke sleutel dat op uw computer is opgeslagen. Het komt overeen met een tekstbestand met dezelfde naam als de openbare sleutel, zonder de extensie &quot;.pub&quot; (bijv. &quot;enable&quot;).

   ![](assets/do-not-localize/connect2.png)

   De **[!UICONTROL Password]** wordt automatisch ingevuld met de persoonlijke sleutel uit het bestand.

   ![](assets/do-not-localize/connect3.png)

   U kunt controleren of de toets die u wilt gebruiken, is opgeslagen in het Configuratiescherm door de vingerafdruk van de persoonlijke of openbare sleutel te vergelijken met de vingerafdruk van de toetsen die worden weergegeven op het tabblad Key Management van de SFTP-kaart.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Als u een Mac-computer gebruikt, kunt u de vingerafdruk van de persoonlijke sleutel die in uw computer is opgeslagen, weergeven door deze opdracht uit te voeren:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Klik op **[!UICONTROL Connect]** om u aan te melden bij uw SFTP-server.

   ![](assets/do-not-localize/sftpconnected.png)
