---
title: SSL-certificaten van subdomeinen controleren
description: Leer hoe u de SSL-certificaten van uw subdomeinen kunt controleren
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# SSL-certificaten van subdomeinen controleren {#monitoring-ssl-certificates}

## SSL-certificaten {#about-ssl-certificates}

Adobe Campaign raadt u aan de subdomeinen te beveiligen die als host dienen voor uw bestemmingspagina&#39;s, in het bijzonder de subdomeinen die vertrouwelijke informatie van uw klanten verzamelen.

**SSL-codering (Secure Socket Layer) zorgt ervoor dat de subdomeinen die u aan Adobe hebt gedelegeerd, veilig zijn.** Wanneer uw klant een webformulier invult of een bestemmingspagina bezoekt die wordt gehost door Adobe Campaign, wordt de informatie standaard verzonden via een niet-beveiligd protocol (HTTP). Om extra veiligheid te verzekeren, veilige verzonden informatie met een protocol HTTPS. Het subdomeinadres &quot;http://info.mywebsite.com/&quot; is nu bijvoorbeeld &quot;https://info.mywebsite.com/&quot;.

**SSL-certificaten worden niet op de gedelegeerde subdomeinen zelf** geïnstalleerd. Zij zijn geïnstalleerd op bijbehorende subdomeinen, hoofdzakelijk die die die landingspagina&#39;s, middelpagina&#39;s en anderen ontvangen.

**SSL-certificaten worden verstrekt voor een specifieke periode** (1 jaar, 60 dagen enz.). Zodra een certificaat verloopt, kunt u problemen ondervinden wanneer u de bestemmingspagina&#39;s opent of middelen van subdomain gebruikt. Om dit te verhinderen, staat het Controlebord u toe om SSL certificaten van uw subdomeinen te controleren, evenals hun vernieuwingsproces in werking te stellen.

![](assets/no_certificate.png)

## SSL-certificaten controleren {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Subdomeindetails"
>abstract="Haal informatie op over de subdomeinen."

De status van de SSL-certificaten van uw subdomeinen is rechtstreeks beschikbaar in de lijst met subdomeinen wanneer u de **[!UICONTROL Subdomains & Certificates]** kaart selecteert.

Subdomeinen worden gerangschikt op de dichtstbijzijnde vervaldatum van het SSL-certificaat, met visuele informatie over de vervaldatum, in dagen:

* **Groen**: het subdomein heeft geen certificaat dat binnen de volgende 60 dagen vervalt.
* **Oranje**: een of meer subdomeinen hebben een certificaat dat binnen de komende 60 dagen zal verlopen.
* **Rood**: een of meer subdomeinen hebben een certificaat dat binnen de komende 30 dagen zal verlopen.
* **Grijs**: er is geen certificaat geïnstalleerd voor het subdomein.

![](assets/subdomains_list.png)

To get more details on a subdomain, click the **[!UICONTROL Subdomain Details]** button.
De lijst met alle verwante subdomeinen wordt weergegeven. Dit omvat doorgaans subdomeinen van bestemmingspagina&#39;s, bronpagina&#39;s, enz.

Het **[!UICONTROL Sender info]** tabblad bevat informatie over de geconfigureerde postvakken (Afzender, Reageren op, Fout-mail).

![](assets/subdomain_details.png)

Als een van de SSL-certificaten van het subdomein bijna verlopen is, kunt u het rechtstreeks vernieuwen via het Configuratiescherm. Raadpleeg voor meer informatie deze sectie: [SSL-certificaat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)van een subdomein vernieuwen.

>[!IMPORTANT]
>
>Certificaatvernieuwing via het Configuratiescherm is beschikbaar in de bètaversie en kan vaak zonder voorafgaande kennisgeving worden bijgewerkt en gewijzigd.

**Verwante onderwerpen:**

* [SSL-certificaten toevoegen (zelfstudie video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [SSL-certificaat van een subdomein vernieuwen](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md)
