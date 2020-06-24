---
title: SFTP-opslagbeheer
description: Leer hoe u de opslag van uw SFTP-server kunt controleren en beheren
translation-type: tm+mt
source-git-commit: d8fe1c2e847fa25919f81bf0a4195de5ad0b2781
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 3%

---


# SFTP-opslagbeheer {#sftp-storage-management}

>[!CONTEXTUALHELP]
>id="cp_storage"
>title="Opslagcapaciteit"
>abstract="Op dit tabblad kunt u de opslagcapaciteit en de gebruiksgegevens voor uw SFTP-servers weergeven. Alleen SFTP-servers waartoe u toegang hebt, worden hier weergegeven. Neem contact op met uw beheerder om toegang tot andere SFTP-servers aan te vragen."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4" text="Video over demo bekijken"

Afhankelijk van uw contractvoorwaarden beschikt u mogelijk over verschillende opslagcapaciteit die op uw SFTP-server is ingericht.

Het is van essentieel belang dat u regelmatig de beschikbare ruimte voor elk van uw SFTP-servers controleert. Anders kunt u mogelijk geen extra bestanden meer opslaan op de server of kunt u geen workflows uitvoeren die afhankelijk zijn van de updates van deze server.

**Verwante onderwerpen:**

* [Campaign Standard-zelfstudievideo](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/monitoring-server-capacity-allow-listing-adding-ssh-key.html)
* [Campaign Classic-zelfstudievideo](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/monitoring-server-capacity-allow-listing-adding-ssh-key.html)

## Toegang tot opslagcapaciteitsinformatie {#accessing-storage-capacity-information}

Informatie over de ruimte die wordt gebruikt door alle instanties tot u toegang hebt, is beschikbaar op het **[!UICONTROL Storage]** tabblad van de SFTP-kaart. Deze wordt bijgewerkt op elke pagina die wordt vernieuwd.

![](assets/control_panel_space.png)

Voor elke instantie, laat een visuele alarm u weten wanneer zijn opslag zijn capaciteit overtreft:

* **Oranje**: de instantie meer dan 80% van haar capaciteit bedraagt,
* **Rood**: de instantie overtreft 90 % van haar capaciteit .

Er zijn ook extra tips beschikbaar om u te helpen te weten hoe u verder kunt gaan terwijl uw server de capaciteit bijna heeft.

## Aanbevolen procedures wanneer de opslagcapaciteit bijna leeg is {#best-practices-when-capacity-runs-out}

1. **Reinig de server SFTP van oude of onnodige dossiers**. Raadpleeg [deze sectie](../../sftp/using/logging-into-sftp-server.md)voor meer informatie over het openen van de SFTP-servermap.
1. Zorg ervoor dat de **workflows** die uw SFTP-servers opschonen met succes worden uitgevoerd. Raadpleeg de speciale documentatie van [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) en [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) voor meer informatie over technische workflows in Adobe Campaign.
1. Neem contact op met uw accountteam om meer opslagruimte **** aan te vragen (hiervoor worden mogelijk extra kosten in rekening gebracht).
1. Neem contact op met de **Klantenservice** als u denkt dat er een probleem is.
