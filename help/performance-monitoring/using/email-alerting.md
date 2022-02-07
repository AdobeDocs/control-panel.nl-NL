---
product: campaign
solution: Campaign
title: E-mailwaarschuwingen
description: Leer hoe u e-mailmeldingen kunt ontvangen in geval van problemen met uw campagneexemplaren
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: ec83878e93536c979c39da52ed07b465f4fbbcb1
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# E-mailwaarschuwingen {#email-alerting}

Voor meer flexibiliteit in uw werk is het Configuratiescherm uitgerust met de functionaliteit voor realtime e-mailwaarschuwingen.

Voer de volgende stappen uit om u te abonneren op deze waarschuwingen:

1. Klik op de knop **[!UICONTROL Alerting notifications]** klikt u op een willekeurige locatie in het Configuratiescherm en vervolgens op **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Er wordt een e-mail verzonden ter bevestiging van uw abonnement.

   ![](assets/email_subscription.png)

1. Nadat u zich hebt geabonneerd, geeft het Configuratiescherm een melding over systeemproblemen en worden de acties aanbevolen die moeten worden uitgevoerd. E-mailwaarschuwingen worden verzonden naar iedereen die zich heeft aangemeld voor **alle instanties** dat zij administrateurs van zijn.

   ![](assets/alert_sample.png)

De lijst van signaleringen ziet er als volgt uit:

* **Opslaggebruik SFTP**: Een van uw SFTP-servers heeft 80% of meer van de capaciteit bereikt. Zie [SFTP-opslagbeheer](../../sftp/using/sftp-storage-management.md).

* **Databasegebruik**: Een van de databases van uw instanties heeft 80% of meer van de capaciteit bereikt. Zie [Bewaking van databases](../../performance-monitoring/using/database-monitoring.md).

* **verlopen SSL-certificaat**: Een van de SSL-certificaten van uw subdomeinen is verlopen of verloopt over 60 dagen of minder. Zie [SSL-certificaten van subdomeinen controleren](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

* **SFTP IP staat het verlopen van de lijst toe**: Één van de IP waaiers u bepaalde is verlopen of zal in 10 dagen of minder verlopen. Zie [Aanbieding in IP-bereik toegestaan](../../sftp/using/ip-range-allow-listing.md).

* **Vervaldatum openbare sleutel SFTP**: Een van de openbare sleutels die u hebt gedefinieerd, is verlopen of verloopt over tien dagen of minder. Zie [Sleutelbeheer](../../sftp/using/key-management.md).

* **Lange lopende Vragen**: Een query wordt al meer dan 24 uur uitgevoerd op een van uw instanties. Zie [Actieve query&#39;s controleren](database-active-queries.md).