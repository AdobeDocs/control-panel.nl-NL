---
product: campaign
solution: Campaign
title: SFTP-opslagbeheer
description: Leer hoe u de opslag van uw SFTP-server kunt controleren en beheren
feature: Control Panel
role: Architect
level: Experienced
exl-id: eaf67573-f088-47d9-8a25-273d08dc541a
source-git-commit: cca04cd965c00a9e2bc496de632ee41ce53a166a
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 90%

---

# SFTP-opslagbeheer {#sftp-storage-management}

>[!CONTEXTUALHELP]
>id="cp_storage"
>title="Opslagcapaciteit"
>abstract="Op dit tabblad kunt u de opslagcapaciteit en de gebruiksgegevens voor uw SFTP-servers weergeven. Alleen SFTP-servers waartoe u toegang hebt, worden hier weergegeven. Neem contact op met uw beheerder om toegang tot andere SFTP-servers aan te vragen."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4" text="Demovideo bekijken"

Afhankelijk van uw contractvoorwaarden is mogelijk andere opslagcapaciteit op uw SFTP-server ingericht.

Het is van essentieel belang dat u regelmatig de beschikbare ruimte voor al uw SFTP-servers controleert. Anders kunt u mogelijk geen bestanden meer opslaan op de server of kunt u geen workflows uitvoeren die afhankelijk zijn van de updates van deze server.

![](assets/do-not-localize/how-to-video.png) Deze functie in video ontdekken met [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/monitoring-server-capacity.html#sftp-management) of [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/monitoring-server-capacity.html#sftp-management).

## Informatie over opslagcapaciteit weergeven {#accessing-storage-capacity-information}

Informatie over de ruimte die wordt gebruikt door alle instanties waartoe u toegang hebt, is beschikbaar op het tabblad **[!UICONTROL Storage]** van de SFTP-kaart. Deze informatie wordt bijgewerkt telkens wanneer de pagina wordt vernieuwd.

![](assets/control_panel_space.png)

Voor elke instantie wordt met een visueel signaal aangegeven wanneer de opslagcapaciteit wordt overschreden:

* **Oranje**: de instantie gebruikt meer dan 80% van de capaciteit.
* **Rood**: de instantie gebruikt meer dan 90% van de capaciteit.

Er zijn ook extra tips beschikbaar om u te adviseren wat u moet doen wanneer de grens van de servercapaciteit bijna is bereikt.

## Aanbevolen procedures wanneer de grens van de opslagcapaciteit wordt bereikt {#best-practices-when-capacity-runs-out}

1. **Verwijder oude of onnodige bestanden van de SFTP-server**. Raadpleeg [deze sectie](../../sftp/using/logging-into-sftp-server.md) voor meer informatie over het openen van de SFTP-servermap.
1. Zorg ervoor dat de **workflows** die uw SFTP-servers opschonen, correct worden uitgevoerd. Raadpleeg de speciale documentatie van [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html) en [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html) voor meer informatie over technische workflows in Adobe Campaign.
1. Neem contact op met uw accountteam om **meer opslagruimte aan te vragen** (hiervoor worden mogelijk extra kosten in rekening gebracht).
1. Neem contact op met de **Klantenservice** als u denkt dat er een probleem is.
