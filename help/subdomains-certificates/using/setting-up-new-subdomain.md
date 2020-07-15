---
title: Een nieuw subdomein instellen
description: Leer hoe u een nieuw subdomein voor uw Campaign-instanties instelt
translation-type: ht
source-git-commit: 5b7e8126789690662e72e72c885700b971362004
workflow-type: ht
source-wordcount: '995'
ht-degree: 100%

---


# Een nieuw subdomein instellen {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Nieuwe subdomeinen instellen en certificaten beheren"
>abstract="U moet een nieuw subdomein instellen en de SSL-certificaten van uw subdomeinen beheren voordat u e-mails kunt verzenden of landingspagina’s kunt publiceren met Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/nl-NL/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="SSL-certificaten van uw subdomeinen bewaken"

>[!IMPORTANT]
>
>Delegatie van subdomeinen vanuit het Configuratiescherm is beschikbaar in de bètaversie en kan regelmatig worden bijgewerkt en gewijzigd zonder kennisgeving.

## Volledige subdomeindelegatie {#full-subdomain-delegation}

Met het Configuratiescherm kunt u een subdomein volledig delegeren aan Adobe Campaign. Ga als volgt te werk om dit te doen:

1. Selecteer in de kaart **[!UICONTROL Subdomains & Certificates]** de gewenste productie-instantie en klik op **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >Subdomeindelegatie is alleen beschikbaar voor **productie**-instanties.
   >
   >Als de geselecteerde instantie geen eerder geconfigureerde subdomeinen heeft, wordt het eerste subdomein dat aan Adobe is gedelegeerd, het **primaire subdomein** voor die instantie. U kunt dit later niet meer wijzigen. Omgekeerde DNS-records worden gemaakt voor andere subdomeinen die het primaire subdomein gebruiken. Antwoordadressen en adressen voor retourzending voor andere subdomeinen worden op basis van het primaire subdomein gegenereerd.

1. Klik op **[!UICONTROL Next]** om de methode voor volledige delegatie te bevestigen.

   Houd er rekening mee dat [CNAME](#use-cnames) en aangepaste methodes momenteel niet door het Configuratiescherm worden ondersteund.

   ![](assets/subdomain3.png)

1. Maak het gewenste subdomein en naamservers in de hostingoplossing die door uw organisatie wordt gebruikt. Daarvoor kopieert u de weergegeven informatie van de Adobe-naamserver en plakt u deze in de wizard. Raadpleeg de [videotutorial](https://video.tv.adobe.com/v/30175?captions=dut) voor meer informatie over het maken van een subdomein in een hostingoplossing.

   >[!IMPORTANT]
   >
   >Wanneer u naamservers configureert, mag u het hoofdsubdomein **nooit aan Adobe delegeren**. Anders werkt het domein alleen met Adobe. Elk ander gebruik is onmogelijk, zoals bijvoorbeeld het verzenden van interne e-mails naar de werknemers van uw organisatie.
   >
   >Bovendien mag u **geen afzonderlijk zonebestand maken** voor dit nieuwe subdomein.

   ![](assets/subdomain4.png)

1. Wanneer het subdomein is gemaakt met de bijbehorende Adobe-naamservergegevens, klikt u op **[!UICONTROL Next]**.

1. Selecteer hoe u het subdomein wilt gebruiken:

   * **Marketing communications**: Communicatie die voor commerciële doeleinden is bestemd. Voorbeeld: e-mailcampagne voor verkoop.
   * **Transactional &amp; operational communications**: Transactionele communicatie bevat informatie gericht op de voltooiing van een proces dat de ontvanger met u is begonnen. Voorbeeld: koopbevestiging, e-mail voor opnieuw instellen van wachtwoord. Operationele communicatie betreft de uitwisseling van informatie, ideeën, en meningen binnen en buiten de organisatie, zonder commercieel doel.
   ![](assets/subdomain5.png)

   **Met het oog op bezorgbaarheid kunt u uw subdomeinen het beste onderverdelen op basis van gebruiksscenario’s**. Hierdoor wordt de reputatie van elk subdomein geïsoleerd en beschermd. Als uw subdomein bijvoorbeeld voor marketingmededelingen door internetproviders wordt toegevoegd aan de lijst van afgewezen domeinen, wordt uw subdomein voor transactionele communicatie niet beïnvloed en kan dit subdomein nog steeds mededelingen verzenden.

   **U kunt subdomeinen voor zowel marketing- als transactionele gebruiksscenario’s delegeren**:

   * Bij marketinggebruiksscenario’s worden subdomeinen geconfigureerd op **MID**-instanties (Mid-sourcing).
   * Voor transactionele gebruiksscenario’s worden subdomeinen geconfigureerd op ALLE **RT**-instanties (Message Center/Real-time messaging) om connectiviteit te verzekeren. De subdomeinen werken daarom met al uw RT-instanties.
   >[!NOTE]
   >
   >Als u Campaign Classic gebruikt, kunt u in het Configuratiescherm zien welke RT-/MID-instanties zijn verbonden met de marketinginstantie waarmee u werkt. Raadpleeg voor meer informatie de sectie [Instantiedetails](../../instances-settings/using/instance-details.md).

1. Voer het subdomein in dat u in uw hostingoplossing hebt gemaakt en klik op **[!UICONTROL Submit]**.

   Zorg ervoor dat u de **volledige naam** invult van het subdomein dat u wilt delegeren. Als u bijvoorbeeld het subdomein usoffers.email.weretail.com wilt delegeren, typt u &#39;usoffers.email.weretail.com&#39;.

   ![](assets/subdomain6.png)

1. Nadat het subdomein is ingediend, controleert het Configuratiescherm of het correct verwijst naar Adobe NS-records en of de SOA-record (Start of Authority) bestaat voor dit subdomein.

   >[!NOTE]
   >
   >Terwijl de subdomeindelegatie wordt uitgevoerd, worden andere verzoeken via het Configuratiescherm in een wachtrij geplaatst en pas uitgevoerd nadat de subdomeindelegatie is voltooid, om prestatieproblemen te voorkomen.

1. Als de controles slagen, worden DNS-records, extra URL’s, inboxes, enz., voor het subdomein ingesteld.

   ![](assets/subdomain7.png)

   Uiteindelijk wordt het **Afleverteam** over het nieuwe subdomein geïnformeerd, om het te controleren. Het controleproces kan tot 10 werkdagen duren nadat het subdomein is gedelegeerd. De controles die worden uitgevoerd, omvatten het testen van feedbackloops en spamklachtloops. U kunt het subdomein daarom beter niet gebruiken voordat de controle is voltooid, aangezien dit in slechte subdomeinreputatie zou kunnen resulteren.

   Klik op de knop **[!UICONTROL Process details]** voor meer details over de configuratievooruitgang.

   ![](assets/subdomain_audit.png)

   **Problemen oplossen:**

   * In sommige gevallen wordt het delegatieproces uitgevoerd maar mislukt de controle van het subdomein. Het subdomein blijft in de lijst **[!UICONTROL Configured]** staan met een taaklog dat informatie over de fout bevat. Neem contact op met de klantenservice als u het probleem niet kunt oplossen.
   * Als het subdomein als Unverified wordt weergegeven nadat het is geconfigureerd, start u een nieuwe subdomeincontrole (**...**/**[!UICONTROL Verify subdomain]**). Als nog steeds dezelfde status wordt weergegeven, is er mogelijk een wijziging in het ontvangersschema aangebracht die niet kan worden gecontroleerd met standaardprocessen. Probeer een campagne met dat subdomein te verzenden.
   * Als de leveringscontrolefase van de subdomeinconfiguratie te lang (meer dan 10 werkdagen) duurt, neemt u contact op met de klantenservice.

Aan het einde van het proces zijn de subdomeinen geconfigureerd voor uw Adobe Campaign-instantie en zijn de onderstaande elementen gemaakt:

* **Het subdomein met de volgende DNS-records**: SOA, MX, CNAME(’s), DKIM, SPF, TXT
* **Aanvullende subdomeinen** voor het hosten van spiegel-, resource- en trackingpagina’s en de domeinsleutel
* **Inboxes**: Sender, Error, Reply-to

   Standaard is de inbox Reply-to in het Configuratiescherm geconfigureerd voor het wissen van e-mailberichten en kan deze niet worden weergegeven. Gebruik dit adres niet als u de inbox Reply-to voor uw marketingcampagnes wilt bewaken.

Klik op de knoppen **[!UICONTROL Subdomain details]** en **[!UICONTROL Sender info]** voor meer details over het subdomein.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Gebruik van CNAME’s {#use-cnames}

Het gebruik van CNAME’s voor subdomeindelegatie wordt niet ondersteund door het Configuratiescherm. Neem contact op met de klantenservice van Adobe als u deze methode wilt gebruiken.

**Verwante onderwerpen:**

* [Subdomeinen delegeren (videotutorial)](https://docs.adobe.com/content/help/nl-NL/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md)
* [Uw subdomeinen bewaken](../../subdomains-certificates/using/monitoring-subdomains.md)