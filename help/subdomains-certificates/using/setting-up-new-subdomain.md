---
product: campaign
solution: Campaign
title: Een nieuw subdomein instellen
description: Leer hoe u een nieuw subdomein voor uw Campaign-instanties instelt
feature: Control Panel
role: Architect
level: Experienced
exl-id: d92781c3-14cc-4716-a131-580ccff46d6e
source-git-commit: 503280181293df6ec5ffaf6c148042d54c5c1958
workflow-type: tm+mt
source-wordcount: '1523'
ht-degree: 80%

---


# Een nieuw subdomein instellen {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Nieuwe subdomeinen instellen en certificaten beheren"
>abstract="U moet een nieuw subdomein instellen en de SSL-certificaten van uw subdomeinen beheren voordat u e-mails kunt verzenden of landingspagina’s kunt publiceren met Adobe Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=nl" text="SSL-certificaten bewaken"

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="SSL-certificaten van subdomeinen delegeren aan Adobe"
>abstract="Met het Configuratiescherm kunt u SSL-certificaten van uw subdomeinen laten beheren door Adobe. Als u CNAMEs aan opstelling gebruikt uw subdomain, zullen de certificaatverslagen automatisch worden geproduceerd en verstrekt om een certificaat in uw domein te produceren ontvangende oplossing. Deze mogelijkheid is alleen beschikbaar wanneer u een nieuw subdomein instelt. U kunt geen certificaten delegeren voor bestaande gedelegeerde subdomeinen."

## Lees hier meer {#must-read}

Deze pagina biedt informatie over het instellen van nieuwe subdomeinen met volledige subdomeindelegatie of CNAMEs Algemene concepten voor deze twee methoden worden in dit gedeelte beschreven: [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md).

**Verwant onderwerp:**

* [Uw subdomeinen controleren](../../subdomains-certificates/using/monitoring-subdomains.md)

### Versieselectie

Subdomeinconfiguratie is alleen beschikbaar voor **productie** versies.

Als de versie die u in de wizard selecteert, geen eerder ingestelde subdomeinen heeft, wordt het eerste geconfigureerde subdomein het **primaire subdomein** voor die versie en kunt u dit in de toekomst niet meer wijzigen. Als gevolg hiervan worden **reverse DNS-records** gemaakt voor andere subdomeinen die dit primaire subdomein gebruiken. **Antwoord- en bounce-adressen** voor andere subdomeinen worden gegenereerd vanuit het primaire subdomein.

### Configuratie naamservers

Wanneer u naamservers configureert, mag u het hoofdsubdomein **nooit aan Adobe delegeren**. Anders werkt het domein alleen met Adobe. Elk ander gebruik is onmogelijk, zoals bijvoorbeeld het verzenden van interne e-mails naar de werknemers van uw organisatie.

Bovendien mag u **geen afzonderlijk zonebestand maken** voor dit nieuwe subdomein.

## Volledige subdomeindelegatie {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="cp_add_new_subdomain"
>title="Nieuw subdomein toevoegen"
>abstract="Adobe beveelt volledige subdomeindelegatie aan. U kunt echter CNAME&#39;s of aangepaste methoden gebruiken om subdomeinen in te stellen."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=nl" text="Een nieuw subdomein instellen"
>additional-url="https://helpx.adobe.com/nl/enterprise/using/support-for-experience-cloud.html" text="Contact opnemen met de klantenservice"


>[!CONTEXTUALHELP]
>id="cp_add_subdomain_create_delegate"
>title="Subdomein maken en delegeren"
>abstract="Maak het subdomein dat u met Adobe Campaign wilt gebruiken, in uw hostingoplossing en delegeer het aan Adobe."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=nl" text="Een nieuw subdomein instellen"

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_submit"
>title="Subdomein verzenden"
>abstract="Bevestig en verzend het subdomein dat in de vorige stappen is gevormd."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=nl" text="Een nieuw subdomein instellen"

Volg de onderstaande stappen om een subdomein volledig te delegeren aan Adobe Campaign.

![](assets/do-not-localize/how-to-video.png) Een video-uitleg van deze functie met [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=nl#subdomains-and-certificates?lang=nl) of [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=nl#subdomains-and-certificates?lang=nl).

1. Selecteer in de kaart **[!UICONTROL Subdomains & Certificates]** de gewenste productieversie en klik op **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

1. Klik op **[!UICONTROL Next]** om de methode voor volledige delegatie te bevestigen.

   ![](assets/subdomain3.png)

1. Maak het gewenste subdomein en naamservers in de hostingoplossing die door uw organisatie wordt gebruikt. Daarvoor kopieert u de weergegeven informatie van de Adobe-naamserver en plakt u deze in de wizard. Raadpleeg de [videotutorial](https://video.tv.adobe.com/v/30175) voor meer informatie over het maken van een subdomein in een hostingoplossing.

   >[!NOTE]
   >
   > Voor Adobe Campaign Standard kunt u met gedelegeerde subdomeinen zowel **Marketing-** als **Transactionele** communicatie verzenden.

   ![](assets/subdomain4.png)

1. Klik op **[!UICONTROL Next]** wanneer het subdomein is gemaakt met de bijbehorende naamserverinformatie van Adobe.

1. Als u een Campagne v7/v8-instantie hebt geselecteerd, selecteert u het gewenste gebruiksgeval voor het subdomein: **Marketingsmededelingen** of **Transactionele en operationele communicatie**. Algemene concepten in de gebruiksscenario&#39;s van subdomeinen worden weergegeven in [dit gedeelte](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/subdomain5.png)

1. Voer het subdomein in dat u in uw hostingoplossing hebt gemaakt en klik op **[!UICONTROL Submit]**.

   Zorg ervoor dat u de **volledige naam** invult van het subdomein dat u wilt delegeren. Als u bijvoorbeeld het subdomein usoffers.email.weretail.com wilt delegeren, typt u &#39;usoffers.email.weretail.com&#39;.

1. Als u de generatie van het SSL-certificaat van het subdomein wilt delegeren aan Adobe, schakelt u het **[!UICONTROL Opt for Adobe managed SSL for sub-domains]** optie.

   ![](assets/subdomain6.png)

Nadat het subdomein is verzonden, worden verschillende controles en configuratiestappen  uitgevoerd door het configuratiescherm. Zie voor meer informatie [Controles en configuratie van subdomeinen](#subdomain-checks-and-configuration).

## Subdomeinconfiguratie met gebruik van CNAME {#use-cnames}

>[!CONTEXTUALHELP]
>id="cp_add_cname_subdomain_create_delegate"
>title="Subdomein configureren"
>abstract="Geef in dit scherm het subdomein op dat u wilt configureren met behulp van CNAME&#39;s."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=nl" text="Een nieuw subdomein instellen"

>[!CONTEXTUALHELP]
>id="cp_add_cname_records"
>title="Records genereren"
>abstract="Navigeer naar uw hostingoplossing om de lijst met DNS-records te genereren die in dit scherm wordt weergegeven."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=nl" text="Een nieuw subdomein instellen"

>[!CONTEXTUALHELP]
>id="cp_add_cname_subdomain_submit"
>title="Subdomein verzenden"
>abstract="Bevestig en verzend het subdomein dat in de vorige stappen is gevormd."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=nl" text="Een nieuw subdomein instellen"

Volg de onderstaande stappen om een subdomein te configureren met gebruik van CNAMEs.

![](assets/do-not-localize/how-to-video.png) Een video-uitleg van deze functie met [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=nl) of [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=nl).

1. Selecteer in de kaart **[!UICONTROL Subdomains & Certificates]** de gewenste productieversie en klik op **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

1. Selecteer de methode **[!UICONTROL CNAME]** en klik op **[!UICONTROL Next]**.

   ![](assets/cname-method-selection.png)

1. Als u een Campagne v7/v8-instantie hebt geselecteerd, selecteert u het gewenste gebruiksgeval voor het subdomein: **Marketingsmededelingen** of **Transactionele en operationele communicatie**. Algemene concepten in de gebruiksscenario&#39;s van subdomeinen worden weergegeven in [dit gedeelte](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/cname-use-case.png)

1. Ga subdomain in die u in uw het ontvangen oplossing creeerde. Als u de generatie van het SSL-certificaat van het subdomein wilt delegeren aan Adobe, schakelt u het **[!UICONTROL Opt for Adobe managed SSL for sub-domains]** optie.

   ![](assets/cname-adobe-managed.png)

   >[!NOTE]
   >
   >Zorg ervoor dat u de **volledige naam** invult van het subdomein dat u wilt instellen. Als u bijvoorbeeld het subdomein usoffers.email.weretail.com wilt instellen, typt u usoffers.email.weretail.com.

1. De lijst van records die in uw DNS-serverweergaven moeten worden geplaatst. Kopieer deze records één voor één of download een CSV-bestand en navigeer vervolgens naar uw domeinhostingoplossing om de overeenkomende DNS-records te genereren.

   ![](assets/cname-generate-record.png)

1. Zorg ervoor dat alle DNS-records van vorige stappen zijn gegenereerd in uw domeinhostingoplossing. Als alles goed is geconfigureerd, selecteert u de eerste statement en klikt u op **[!UICONTROL Next]** om te bevestigen.

   Als u de records wilt maken en de subdomeinconfiguratie later wilt verzenden, selecteert u de tweede instructie. U kunt dan de subdomeinconfiguratie direct vanuit het subdomeinbeheerschermgebied **[!UICONTROL Processing]** hervatten. Houd er rekening mee dat DNS-records die op uw server worden geplaatst, 30 dagen door het configuratiescherm worden bewaard. Na die periode moet u het subdomein helemaal opnieuw configureren.


   >[!NOTE]
   >
   >Als u verkoos om het SSL certificaat niet aan Adobe te delegeren, is dit de laatste stap van de subdomeinconfiguratie. Klik op de knop **[!UICONTROL Submit]**.

   ![](assets/cname-confirmation.png)

1. Als u het certificaat van de subdomeinen aan Adobe wilt delegeren, worden de certificaatverslagen automatisch geproduceerd. Kopieer deze records, een voor een of door een CSV-bestand te downloaden, en navigeer vervolgens naar de oplossing voor domeinhosting om het overeenkomende certificaat te genereren.

   ![](assets/cname-csr-generation.png)

1. Zorg ervoor dat alle certificaatverslagen in uw domein het ontvangen oplossing zijn geproduceerd. Als alles goed is geconfigureerd, selecteert u de eerste statement en klikt u op **[!UICONTROL Submit]** om te bevestigen.

   ![](assets/cnames-submit.png)

Nadat het subdomein is verzonden, worden verschillende controles en configuratiestappen  uitgevoerd door het configuratiescherm. Zie voor meer informatie [Controles en configuratie van subdomeinen](#subdomain-checks-and-configuration).

## Controles en configuratie van subdomeinen {#subdomain-checks-and-configuration}

1. Zodra een subdomein is verzonden, controleert het configuratiescherm of het correct verwijst naar Adobe NS-records en of de Start of Authority-record (SOA) niet bestaat voor dit subdomein.

   >[!NOTE]
   >
   >Merk op dat terwijl de looppas van de subdomeinconfiguratie, andere verzoeken van het Controlebord in een rij zullen zijn ingegaan en slechts uitgevoerd nadat de subdomeinconfiguratie voltooit, om het even welke prestatieskwesties te verhinderen.

1. Als de controles succesvol zijn, begint het configuratiescherm met het instellen van het subdomein met DNS-records, bijkomende URL&#39;s, inboxen, enz.

   ![](assets/subdomain7.png)

   Voor meer details over de voortgang van de configuratie klikt u op de knop voor de configuratie van het subdomein **[!UICONTROL Details]**.

   ![](assets/subdomain_audit.png)

1. Uiteindelijk wordt het **Afleverteam** over het nieuwe subdomein geïnformeerd om het te controleren. Het auditproces kan tot 10 werkdagen duren nadat het subdomein is geconfigureerd.

   >[!IMPORTANT]
   >
   >De aflevercontroles die worden uitgevoerd, omvatten het testen van feedbackloops en spamklachtloops. We raden daarom af om het subdomein te gebruiken voordat de audit is voltooid, omdat dit kan leiden tot een slechte reputatie van het subdomein.
   >
   >Nochtans, merk op dat u verrichtingen met betrekking tot SSL certificaten op uw subdomain kunt uitvoeren, zelfs als de leverbaarheidscontrole nog wordt verwerkt.

1. Aan het einde van het proces zijn de subdomeinen geconfigureerd voor uw Adobe Campaign-instantie en zijn de onderstaande elementen gemaakt:

   * **Het subdomein met de volgende DNS-records**: SOA, MX, CNAME(’s), DKIM, SPF, TXT
   * **Aanvullende subdomeinen** voor het hosten van spiegel-, resource- en trackingpagina’s en de domeinsleutel
   * **Inboxes**: Sender, Error, Reply-to

   Standaard is de inbox Reply-to in het Configuratiescherm geconfigureerd voor het wissen van e-mailberichten en kan deze niet worden weergegeven. Gebruik dit adres niet als u de inbox Reply-to voor uw marketingcampagnes wilt bewaken.

Klik op de knoppen **[!UICONTROL Subdomain details]** en **[!UICONTROL Sender info]** voor meer details over het subdomein.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Problemen oplossen {#troubleshooting}

* In sommige gevallen verloopt de configuratie van het subdomein goed, maar wordt het subdomein mogelijk niet succesvol geverifieerd. Het subdomein blijft in de lijst **[!UICONTROL Configured]** staan met een taaklog dat informatie over de fout bevat. Neem contact op met de klantenservice als u het probleem niet kunt oplossen.
* Als het subdomein als Unverified wordt weergegeven nadat het is geconfigureerd, start u een nieuwe subdomeincontrole (**...**/**[!UICONTROL Verify subdomain]**). Als nog steeds dezelfde status wordt weergegeven, is er mogelijk een wijziging in het ontvangersschema aangebracht die niet kan worden gecontroleerd met standaardprocessen. Probeer een campagne met dat subdomein te verzenden.
* Als de leveringscontrolefase van de subdomeinconfiguratie te lang (meer dan 10 werkdagen) duurt, neemt u contact op met de klantenservice.
