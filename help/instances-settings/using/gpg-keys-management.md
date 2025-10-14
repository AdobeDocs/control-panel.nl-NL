---
product: campaign
solution: Campaign
title: Beheer van GPG-sleutels
description: Leer hoe u GPG-sleutels beheert voor het coderen en decoderen van gegevens in Adobe Campaign.
feature: Control Panel, Encryption
role: Admin
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: de33a10a168358d0f38ca776fbcd88e0ccf63ce2
workflow-type: tm+mt
source-wordcount: '1205'
ht-degree: 8%

---

# Beheer van GPG-sleutels {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="GPG-toetsen"
>abstract="Op dit tabblad kunt u GPG-sleutels installeren en/of genereren voor een marketinginstantie om gegevens te coderen die vanuit Campagne worden verzonden en binnenkomende gegevens te decoderen."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=nl" text="Prestatiebewaking"

## GPG-codering {#about-gpg-encryption}

Met GPG-codering kunt u uw gegevens beveiligen met behulp van een systeem van paren met openbare en persoonlijke sleutels die de [OpenPGP](https://www.openpgp.org/about/standard/) specificatie.

Zodra uitgevoerd, kunt u inkomende gegevens hebben ontsleuteld en uitgaande gegevens worden gecodeerd alvorens de overdracht voorkomt, om ervoor te zorgen dat zij niet door iedereen zonder een geldig passend zeer belangrijk paar zullen worden betreden.

Als u GPG-codering wilt implementeren met Campaign, moeten de GPG-sleutels rechtstreeks vanuit het Configuratiescherm op een marketinginstantie worden geïnstalleerd en/of gegenereerd door een beheerder.

Dan kunt u:

* **Verzonden gegevens versleutelen**: Adobe Campaign verzendt gegevens nadat deze met de geïnstalleerde openbare sleutel zijn gecodeerd.

* **Binnenkomende gegevens decoderen**: Adobe Campaign ontvangt gegevens die van een extern systeem zijn versleuteld met een openbare sleutel die u hebt gedownload van het Configuratiescherm. Adobe Campaign decodeert de gegevens met een persoonlijke sleutel die via het Configuratiescherm wordt gegenereerd.

## Gegevens versleutelen {#encrypting-data}

Met het Configuratiescherm kunt u gegevens versleutelen die afkomstig zijn van uw Adobe Campaign-instantie.

Hiervoor moet u een GPG-sleutelpaar genereren van een PGP-versleutelingsprogramma en vervolgens de openbare sleutel installeren in het Configuratiescherm. Vervolgens kunt u gegevens versleutelen voordat u deze vanuit uw instantie verzendt. Volg de onderstaande stappen om dit te doen.

>[!NOTE]
>
>U kunt maximaal 60 GPG-toetsen installeren in het regelpaneel.

![](assets/do-not-localize/how-to-video.png) [&#x200B; Ontdek deze functie in video](#video)

1. Genereer een combinatie van openbare/persoonlijke sleutels met een PGP-coderingsprogramma volgens de [OpenPGP-specificatie](https://www.openpgp.org/about/standard/). Hiertoe installeert u een GPG-hulpprogramma of GNuGP-software.

   >[!NOTE]
   >
   >Er is open-source gratis software beschikbaar om sleutels te genereren. Nochtans, zorg ervoor u de richtlijnen van uw organisatie volgt en het nut van GPG gebruikt door uw organisatie van IT/Veiligheid wordt geadviseerd.

1. Zodra het nut geïnstalleerd is, stel het bevel hieronder, in de Eind van Mac of het bevel van Vensters in werking.

   `gpg --full-generate-key`

1. Geef bij de aanwijzing de gewenste parameters voor de toets op. De vereiste parameters zijn:

   * **sleuteltype**: RSA
   * **sleutellengte**: 3072 - 4096 bits
   * **echte naam** en **mailadres**: Hiermee kunt u bijhouden wie het sleutelpaar heeft gemaakt. Voer een naam en e-mailadres in die aan uw organisatie of afdeling zijn gekoppeld.
   * **opmerking**: als u een label toevoegt aan het opmerkingenveld, kunt u gemakkelijk de sleutel identificeren waarmee uw gegevens worden versleuteld.

     >[!IMPORTANT]
     >
     >Zorg ervoor dat dit veld niet leeg blijft en dat een opmerking wordt ingevuld.

   * **vervaldatum**: Datum of 0 voor geen vervaldatum.
   * **passphrase**

   ![](assets/do-not-localize/gpg_command.png)

1. Als dit eenmaal is bevestigd, genereert het script een sleutel met de bijbehorende vingerafdruk, die u in een bestand kunt exporteren of rechtstreeks in het Configuratiescherm kunt plakken. Als u het bestand wilt exporteren, voert u deze opdracht uit, gevolgd door de vingerafdruk van de sleutel die u hebt gegenereerd.

   `gpg -a --export <fingerprint>`

1. Als u de openbare sleutel in het Configuratiescherm wilt installeren, opent u het dialoogvenster **[!UICONTROL Instance settings]** en selecteert u vervolgens de **[!UICONTROL GPG keys]** en de gewenste instantie.

1. Klik op de knop **[!UICONTROL Install Key]**.

   ![](assets/gpg_install_button.png)

1. Plak de openbare sleutel die is gegenereerd met het PGP-versleutelingsgereedschap. U kunt het geëxporteerde bestand met de openbare sleutel ook rechtstreeks slepen en neerzetten.

   >[!NOTE]
   >
   >De openbare sleutel moet de OpenPGP-indeling hebben.

   ![](assets/gpg_install_paste.png)

1. Klik op de knop **[!UICONTROL Install Key]**.

Zodra de openbare sleutel wordt geïnstalleerd, toont het in de lijst. U kunt de **...** om het te downloaden of zijn vingerafdruk te kopiëren.

![](assets/gpg_install_download.png)

De sleutel is dan beschikbaar voor gebruik in de werkschema&#39;s van Adobe Campaign. U kunt het gebruiken om gegevens te coderen wanneer het gebruiken van gegevens extractieactiviteiten.

![](assets/do-not-localize/how-to-video.png) [&#x200B; Ontdek deze functie in video](#video)

Raadpleeg de documentatie bij Adobe Campaign voor meer informatie over dit onderwerp:

**Campagne v7/v8:**

* [Een bestand zoeken of versleutelen](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=nl-NL)
* [Hoofdlettergebruik: gegevens coderen en exporteren met een sleutel die is geïnstalleerd in het Configuratiescherm](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=nl-NL#use-case-gpg-encrypt)

**Campaign Standard:**

* [Versleutelde data beheren](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=nl-NL)
* [Hoofdlettergebruik: gegevens coderen en exporteren met een sleutel die is geïnstalleerd in het Configuratiescherm](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=nl-NL#use-case-gpg-encrypt)

## Gegevens ontsleutelen {#decrypting-data}

Met het Configuratiescherm kunt u externe gegevens die in Adobe Campaign-instanties komen, decoderen.

Hiervoor moet u een GPG-sleutelpaar rechtstreeks vanuit het Configuratiescherm genereren.

* De **openbare sleutel** wordt gedeeld met het externe systeem, dat het zal gebruiken om de gegevens te coderen die naar Campagne moeten verzenden.
* De **persoonlijke sleutel** wordt gebruikt door Campagne om de inkomende gecodeerde gegevens te decoderen.

![](assets/do-not-localize/how-to-video.png) [&#x200B; Ontdek deze functie in video](#video)

Voer de volgende stappen uit om een sleutelpaar te genereren in het Configuratiescherm:

1. Open de **[!UICONTROL Instance settings]** en selecteert u vervolgens de **[!UICONTROL GPG keys]** en de gewenste Adobe Campaign-instantie.

1. Klik op de knop **[!UICONTROL Generate Key]**.

   ![](assets/gpg_generate.png)

1. Geef de naam van de toets op en klik vervolgens op **[!UICONTROL Generate Key]**. Deze naam helpt u bij het identificeren van de sleutel die moet worden gebruikt voor decodering in Campagneworkflows

   ![](assets/gpg_generate_name.png)

Zodra het zeer belangrijke paar wordt geproduceerd, toont de openbare sleutel in de lijst. De sleutelparen van de decryptie worden geproduceerd zonder vervaldatum.

U kunt de **...** om de openbare sleutel te downloaden of zijn vingerafdruk te kopiëren.

![](assets/gpg_generate_list.png)

De openbare sleutel is dan beschikbaar om met om het even welk extern systeem te worden gedeeld. Adobe Campaign kan de persoonlijke sleutel gebruiken bij het laden van gegevens om gegevens te decoderen die met de openbare sleutel zijn versleuteld.

Raadpleeg de documentatie bij Adobe Campaign voor meer informatie:

**Campagne v7 en v8:**

* [Een bestand uitpakken of decoderen voordat het wordt verwerkt](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=nl-NL)
* [Hoofdlettergebruik: gegevens importeren die zijn versleuteld met een toets die is gegenereerd door het Configuratiescherm](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=nl-NL#use-case-gpg-decrypt)

**Campaign Standard:**

* [Versleutelde data beheren](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=nl-NL)
* [Hoofdlettergebruik: gegevens importeren die zijn versleuteld met een toets die is gegenereerd door het Configuratiescherm](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=nl-NL#use-case-gpg-decrypt)

## GPG-toetsen controleren

Als u toegang wilt tot de GPG-sleutels die zijn geïnstalleerd en gegenereerd voor uw instanties, opent u de **[!UICONTROL Instance settings]** en selecteert u vervolgens de **[!UICONTROL GPG keys]** tab.

![](assets/gpg_list.png)

In de lijst worden alle GPG-sleutels voor versleuteling en ontsleuteling weergegeven die voor uw instanties zijn geïnstalleerd en gegenereerd, met gedetailleerde informatie over elke sleutel:

* **[!UICONTROL Name]**: De naam die is gedefinieerd tijdens het installeren of genereren van de toets.
* **[!UICONTROL Use case]**: In deze kolom wordt het gebruiksgeval van de toets aangegeven:

  ![](assets/gpg_icon_encrypt.png): De sleutel is geïnstalleerd voor gegevenscodering.

  ![](assets/gpg_icon_decrypt.png): De sleutel is gegenereerd voor gegevensdecodering.

* **[!UICONTROL Fingerprint]**: de vingerafdruk van de toets.
* **[!UICONTROL Expires]**: De vervaldatum van de toets. Let op: het Configuratiescherm geeft visuele indicaties als de sleutel de vervaldatum nadert:

   * Dringend (rood) wordt 30 dagen eerder getoond.
   * Waarschuwing (geel) wordt 60 dagen eerder weergegeven.
   * Een &#39;&#39;Verlopen&#39;&#39; rode banner wordt weergegeven zodra een toets is verlopen.

  >[!NOTE]
  >
  >Er wordt geen e-mailmelding verzonden door het regelpaneel.

We raden u aan alle toetsen die u niet meer nodig hebt, te verwijderen. Om dit te doen, klik **...** dan selecteert u **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Voordat u een sleutel verwijdert, moet u ervoor zorgen dat deze niet wordt gebruikt in Adobe Campaign-workflows om te voorkomen dat deze mislukken.

## Video over zelfstudie {#video}

In de onderstaande video ziet u hoe u GPG-sleutels voor gegevenscodering kunt genereren en installeren.

Aanvullende &#39;Hoe kan ik&#39;-video&#39;s over het beheer van GPG-sleutels zijn beschikbaar in  [Campagne v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=nl-NL#instance-settings) en [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=nl-NL#instance-settings) pagina&#39;s met zelfstudies.

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
