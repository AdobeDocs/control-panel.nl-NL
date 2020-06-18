---
title: Aanmelden bij uw SFTP-server
description: Leer hoe u zich aanmeldt bij uw SFTP-server
translation-type: tm+mt
source-git-commit: 3faeb9651681a9edd18cf889fff65b02644cb690
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 2%

---


# Aanmelden bij uw SFTP-server {#logging-into-sft-server}

In de onderstaande stappen wordt beschreven hoe u verbinding kunt maken met uw SFTP-server via uw SFTP-clienttoepassing.

Voordat u zich aanmeldt bij de server, moet u controleren of:

* Uw SFTP-server wordt **gehost door Adobe**.
* Uw **gebruikersnaam** is ingesteld voor de server. You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* U hebt een combinatie van **persoonlijke en openbare sleutels** om u aan te melden bij de SFTP-server. Raadpleeg [deze sectie](../../sftp/using/key-management.md) voor meer informatie over het toevoegen van de SSH-toets.
* Uw **openbare IP adres is toegevoegd aan toestaan lijst** op de server SFTP. Als niet, verwijs naar [deze sectie](../../sftp/using/ip-range-whitelisting.md) voor meer op hoe te om uw IP waaier aan toe te voegen staat lijst toe.
* U hebt toegang tot een **SFTP-clientsoftware**. U kunt uw afdeling van IT voor de cliënttoepassing raadplegen SFTP die zij om adviseren te gebruiken, of onderzoek naar op Internet als dit door uw bedrijfsbeleid wordt toegestaan.

Voer de volgende stappen uit om verbinding te maken met uw SFTP-server:

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]** tab from the **[!UICONTROL SFTP]** card.

   ![](assets/sftp_card.png)

1. Start de SFTP-clienttoepassing en kopieer en plak het serveradres vanuit het Configuratiescherm, gevolgd door &quot;campagne.adobe.com&quot;. Vul vervolgens uw gebruikersnaam in.

   ![](assets/do-not-localize/connect1.png)

1. Selecteer in het **[!UICONTROL SSH Private Key]** veld het bestand met de persoonlijke sleutel dat op uw computer is opgeslagen. Het komt overeen met een tekstbestand met dezelfde naam als de openbare sleutel, zonder de extensie &quot;.pub&quot; (bijv. &quot;enable&quot;).

   ![](assets/do-not-localize/connect2.png)

   Het **[!UICONTROL Password]** veld wordt automatisch ingevuld met de persoonlijke sleutel uit het bestand.

   ![](assets/do-not-localize/connect3.png)

   U kunt controleren of de toets die u wilt gebruiken, is opgeslagen in het Configuratiescherm door de vingerafdruk van de persoonlijke of openbare sleutel te vergelijken met de vingerafdruk van de toetsen die worden weergegeven op het tabblad Key Management van de SFTP-kaart.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Als u een Mac-computer gebruikt, kunt u de vingerafdruk van de persoonlijke sleutel die in uw computer is opgeslagen, weergeven door deze opdracht uit te voeren:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Als alle gegevens zijn ingevuld, klikt u **[!UICONTROL Connect]** om u aan te melden bij uw SFTP-server.

   ![](assets/do-not-localize/sftpconnected.png)
