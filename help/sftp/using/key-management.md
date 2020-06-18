---
title: Sleutelbeheer
description: Leer hoe u sleutels beheert om verbinding te maken met SFTP-servers
translation-type: tm+mt
source-git-commit: 3faeb9651681a9edd18cf889fff65b02644cb690
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 4%

---


# Sleutelbeheer {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="Over sleutelbeheer"
>abstract="Op dit tabblad kunt u de openbare sleutels beheren."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="Video over demo bekijken"

Adobe raadt alle klanten aan verbinding te maken met hun SFTP-servers met een **openbaar/persoonlijk sleutelpaar**.

De stappen om een openbare sleutel van SSH te produceren en het toe te voegen om tot de server toegang te hebben SFTP worden hieronder beschreven, evenals aanbevelingen betreffende authentificatie.

Zodra de toegang tot de server opstelling is, herinner me om de IP adressen **toe te voegen die toegang tot de server aan toestaan lijst** zullen vereisen zodat u met het kunt verbinden. For more on this, refer to [this section](../../instances-settings/using/ip-whitelisting-instance-access.md).

>[!NOTE]
>
>Het is momenteel niet mogelijk om een openbare sleutel van SSH te schrappen.

## Aanbevolen procedures {#best-practices}

**De openbare SSH-toets**

Zorg ervoor dat u altijd dezelfde verificatie gebruikt om verbinding te maken met de server en dat u een ondersteunde indeling voor de sleutel gebruikt.

**API-integratie met gebruikersnaam en wachtwoord**

In zeer zeldzame gevallen wordt op wachtwoord gebaseerde verificatie ingeschakeld op sommige SFTP-servers. Adobe raadt u aan verificatie op basis van sleutels te gebruiken, omdat deze methode efficiënter en veiliger is. U kunt verzoeken om over te schakelen op verificatie op basis van sleutels door contact op te nemen met de klantenservice.

>[!IMPORTANT]
>
>Als uw wachtwoord verloopt, zelfs als er sleutels op uw systeem geïnstalleerd zijn, zult u niet aan uw rekeningen kunnen aanmelden SFTP.

![](assets/control_panel_passwordexpires.png)

## De SSH-toets installeren {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="Nieuwe openbare sleutel toevoegen"
>abstract="Voeg een nieuwe openbare sleutel voor een instantie toe."

>[!IMPORTANT]
>
>De onderstaande stappen zijn een voorbeeld van alleen SSH-sleutelcreatie. Volg de richtlijnen van uw organisatie met betrekking tot SSH-toetsen. Het voorbeeld hieronder is slechts één voorbeeld van hoe dit kan worden gedaan en dient als nuttig referentiepunt voor het communiceren van vereisten aan uw team of interne netwerkgroep.

1. Ga naar het tabblad **[!UICONTROL Key Management]** en klik op de knop **[!UICONTROL Add new public key]**.

   ![](assets/key0.png)

1. Selecteer in het dialoogvenster dat wordt geopend de gebruikersnaam waarvoor u de openbare sleutel wilt maken en de server waarvoor u de sleutel wilt activeren.

   >[!NOTE]
   >
   >De interface controleert of een bepaalde gebruikersnaam actief is op een bepaalde instantie en geeft u een optie om de sleutel in een of meerdere gevallen te activeren.
   >
   >Een of meer openbare SSH-sleutels kunnen voor elke gebruiker worden toegevoegd.

   ![](assets/key1.png)

1. Kopieer de openbare SSH-toets en plak deze. Volg onderstaande stappen voor het genereren van een openbare sleutel:

   >[!NOTE]
   >
   >De openbare sleutel van SSH zou **2048 beetjes** moeten zijn.

   **Linux en Mac:**

   Gebruik Terminal om een openbaar en privé zeer belangrijk paar te produceren:
   1. Voer deze opdracht in: `ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`.
   1. Geef een naam op voor de toets wanneer u hierom wordt gevraagd. Als de .ssh-map niet bestaat, maakt het systeem er een voor u.
   1. Ga, dan reenter, een passphrase in wanneer ertoe aangezet. Het kan ook leeg blijven.
   1. Het systeem maakt een sleutelpaar &quot;name&quot; en &quot;name.pub&quot;. Zoek het bestand &quot;name.pub&quot; en open het. Een alfanumerieke tekenreeks die eindigt met het e-mailadres dat u hebt opgegeven.
   **Windows:**

   Wellicht moet u een hulpprogramma van derden installeren waarmee u persoonlijk/openbaar sleutelpaar in dezelfde indeling als &quot;name.pub&quot; kunt genereren.

1. Open het .pub-bestand en kopieer en plak de hele tekenreeks, te beginnen met &quot;ssh..&quot; in het regelpaneel.

   ![](assets/publickey.png)

1. Klik op de **[!UICONTROL Save]** knop om de toets te maken. In het Configuratiescherm worden de openbare sleutel en de bijbehorende vingerafdruk opgeslagen, gecodeerd met de SHA256-indeling.

U kunt vingerafdrukken gebruiken om de privésleutels die op uw computer zijn opgeslagen, te laten overeenkomen met de overeenkomstige openbare sleutels die in het Configuratiescherm zijn opgeslagen.

![](assets/fingerprint_compare.png)

The &quot;**...**&quot; kunt u een bestaande sleutel verwijderen of de bijbehorende vingerafdruk naar het klembord kopiëren.

![](assets/key_options.png)
