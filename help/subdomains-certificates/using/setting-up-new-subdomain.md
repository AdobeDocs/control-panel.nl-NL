---
title: Een nieuw subdomein instellen
description: Leer hoe u een nieuw subdomein voor uw campagneinstanties instelt
translation-type: tm+mt
source-git-commit: 5b7e8126789690662e72e72c885700b971362004
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 0%

---


# Een nieuw subdomein instellen {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Nieuwe subdomeinen instellen en certificaten beheren"
>abstract="U moet een nieuw subdomein instellen en de SSL-certificaten van uw subdomeinen beheren om e-mails te verzenden of bestemmingspagina&#39;s te publiceren met Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="SSL-certificaten van uw subdomeinen controleren"

>[!IMPORTANT]
>
>De delegatie van subdomeinen van het Controlebord is beschikbaar in bèta, en onderworpen aan regelmatige updates en wijzigingen zonder bericht.

## Volledige subdomeindelegatie {#full-subdomain-delegation}

Met het Configuratiescherm kunt u een subdomein volledig delegeren naar Adobe Campaign. Ga als volgt te werk om dit te doen:

1. Selecteer in de **[!UICONTROL Subdomains & Certificates]** kaart de gewenste productieinstantie en klik op **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >Subdomain delegeren is alleen beschikbaar voor **productie** -instanties.
   >
   >Als de geselecteerde instantie geen eerder geconfigureerde subdomeinen heeft, wordt het eerste subdomein dat aan Adobe is gedelegeerd, het **primaire subdomein** voor die instantie, zodat u dit in de toekomst niet meer kunt wijzigen. Omgekeerde DNS-records worden gemaakt voor andere subdomeinen die het primaire subdomein gebruiken. Antwoord-aan, en stuitadressen voor andere subdomeinen zullen van primaire subdomain worden geproduceerd.

1. Klik **[!UICONTROL Next]** om de volledige delegatiemethode te bevestigen.

   Merk op dat [CNAME](#use-cnames) en douanemethodes momenteel niet door het Controlebord worden gesteund.

   ![](assets/subdomain3.png)

1. Creeer gewenste subdomain en nameservers in de ontvangende oplossing die door uw organisatie wordt gebruikt. Hiervoor kopieert en plakt u de Adobe Nameserver-informatie die in de wizard wordt weergegeven. Raadpleeg de [zelfstudievideo](https://video.tv.adobe.com/v/30175?captions=dut)voor meer informatie over het maken van een subdomein in een hostingoplossing.

   >[!IMPORTANT]
   >
   >Wanneer u nameservers configureert, moet u het hoofdsubdomein **nooit delegeren aan Adobe**. Anders kan het domein alleen met Adobe werken. Elk ander gebruik zal onmogelijk zijn, zoals bijvoorbeeld het verzenden van interne e-mails naar de werknemers van uw organisatie.
   >
   >Maak **bovendien geen afzonderlijk streekbestand** voor dit nieuwe subdomein.

   ![](assets/subdomain4.png)

1. Wanneer het subdomein is gemaakt met de bijbehorende Adobe-servergegevens, klikt u op **[!UICONTROL Next]**.

1. Selecteer het gewenste gebruiksgeval voor het subdomein:

   * **Marketing communicatie**: communicatie die voor commerciële doeleinden is bestemd. Voorbeeld: e-mailcampagne voor verkoop.
   * **Transactionele en operationele communicatie**: transactionele mededelingen bevatten informatie gericht op de voltooiing van een proces dat de ontvanger met u is begonnen. Voorbeeld: aanschafbevestiging, wachtwoord opnieuw instellen e-mail. De organisatorische mededelingen hebben betrekking op de uitwisseling van informatie, ideeën, en meningen binnen en buiten de organisatie, zonder commercieel doel.
   ![](assets/subdomain5.png)

   **U kunt het beste de subdomeinen onderverdelen op basis van de gebruikte gevallen**. Hierdoor wordt de reputatie van elk subdomein geïsoleerd en beschermd. Bijvoorbeeld, als uw subdomein voor marketing mededelingen aan de bloklijst door de Dienstverleners van Internet wordt toegevoegd, zal uw transactie communicatie subdomain niet worden beïnvloed, en zal houden communicatie kunnen verzenden.

   **U kunt subdomeinen voor zowel het Marketing als het Transactionele gebruiksgevallen** delegeren:

   * Bij Gebruiksgevallen voor marketing worden subdomeinen geconfigureerd op **MID** -instanties (medio sourcing).
   * Voor Transactionele gebruiksgevallen, zullen subdomeinen op ALLE instanties van **RT** (het Centrum van het Bericht/Real-time overseinen) worden gevormd om connectiviteit te verzekeren. De subdomeinen zullen daarom met al uw instanties van RT werken.
   >[!NOTE]
   >
   >Als u Campaign Classic gebruikt, kunt u in het Configuratiescherm zien welke RT/MID-instanties zijn verbonden met de marketinginstantie waarmee u werkt. Raadpleeg voor meer informatie de sectie [Instantiedetails](../../instances-settings/using/instance-details.md) .

1. Ga subdomain in die u in uw het ontvangen oplossing creeerde, dan klik **[!UICONTROL Submit]**.

   Zorg ervoor u de **volledige naam** van subdomain aan afgevaardigde invult. Als u bijvoorbeeld het subdomein &quot;usaanbiedingen.email.weretail.com&quot; wilt delegeren, typt u &quot;usaanbiedingen.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Nadat het subdomein is verzonden, controleert het Configuratiescherm of het correct verwijst naar Adobe NS-records en of de SOA-record (Start of Authority) niet bestaat voor dit subdomein.

   >[!NOTE]
   >
   >Merk op dat terwijl de subdomain delegatie looppas, andere verzoeken door het Controlebord in een rij zullen zijn ingegaan en slechts uitgevoerd nadat de Delegatie Subdomain voltooit, om het even welke prestatieskwesties te verhinderen.

1. Als de controles succesvol zijn, zal het Controlebord beginnen vestiging subdomain met DNS verslagen, extra URLs, inboxes etc.

   ![](assets/subdomain7.png)

   Uiteindelijk, zal het team **van de** Levering over nieuw subdomain worden geïnformeerd, om het te controleren. Het controleproces kan tot 10 werkdagen duren nadat het subdomein is gedelegeerd. De controles die worden uitgevoerd omvatten terugkoppelt lijnen en het testen van de spamklachtenlijnen. Daarom adviseren wij niet subdomain te gebruiken alvorens de controle is voltooid, aangezien het in slechte subdomain reputatie zou kunnen resulteren.

   U kunt meer details over de configuratievooruitgang krijgen door de **[!UICONTROL Process details]** knoop te klikken.

   ![](assets/subdomain_audit.png)

   **Problemen oplossen:**

   * In sommige gevallen wordt het delegeren doorlopen, maar is het mogelijk dat het subdomein niet is geverifieerd. Het subdomein blijft in de **[!UICONTROL Configured]** lijst met een taaklogboek dat informatie over de fout bevat. Neem contact op met de klantenservice als het probleem niet is opgelost.
   * Als subdomain als &quot;Niet geverifieerd&quot;na wordt getoond wordt gevormd, lanceer een nieuwe subdomeincontrole (**...** / **[!UICONTROL Verify subdomain]**). Als het nog het zelfde statuut toont, zou de reden kunnen zijn dat er één of andere aanpassing op ontvangersschema wordt gedaan, dat niet kan worden geverifieerd gebruikend standaardprocessen. Probeer een campagne met dat subdomein te verzenden.
   * Als de subdomeinconfiguratie te lang (meer dan 10 werkdagen) bij de stap van de leveringscontrole duurt, gelieve de Zorg van de Klant te bereiken.

Aan het einde van het proces worden de subdomeinen geconfigureerd voor uw Adobe Campaign-instantie en worden de onderstaande elementen gemaakt:

* **Het subdomein met de volgende DNS-records**: SOA, MX, CNAME(S), DKIM, SPF, TXT,
* **Aanvullende subdomeinen** voor het hosten van spiegels, bronnen, trackingpagina&#39;s en domeinsleutel
* **Postvakken**: Afzender, Fout, Reageren op.

   Standaard is de inbox &quot;Reageren op&quot; in het Configuratiescherm geconfigureerd voor het wissen van e-mailberichten en kan deze niet worden weergegeven. Gebruik dit adres niet als u het postvak &quot;Reageren op&quot; voor uw marketingcampagnes wilt controleren.

U kunt meer details op subdomain krijgen door de **[!UICONTROL Subdomain details]** en **[!UICONTROL Sender info]** knopen te klikken.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Gebruik van CNAME&#39;s {#use-cnames}

Het gebruik van CNAMEs voor subdomain delegatie wordt niet gesteund door het Controlebord. Neem contact op met de klantenservice van Adobe als u deze methode wilt gebruiken.

**Verwante onderwerpen:**

* [Subdomeinen delegeren (videozelfstudie)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md)
* [De subdomeinen controleren](../../subdomains-certificates/using/monitoring-subdomains.md)