---
title: Nieuwste release
description: Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen van het Configuratiescherm
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '148'
ht-degree: 100%

---

# Nieuwste release {#control-panel-releases}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen van het configuratiescherm.

## Oktober 2023 {#october-2023}

**Gebruikersinterface**

* Het Configuratiescherm is nu beschikbaar in andere talen. [Meer informatie](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Bewaking van actieve profielen**

* U kunt nu het aantal actieve profielen controleren waarop uw organisatie recht heeft, en het totale aantal profielen dat binnen uw organisatie wordt gebruikt in alle instanties, als u meerdere instanties gebruikt. [Meer informatie](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC-records**

* Meerdere e-mailadressen kunnen nu e-mails met samengevoegde rapporten en foutrapporten ontvangen. [Meer informatie](../subdomains-certificates/using/dmarc.md)
* Er zijn wijzigingen aangebracht als er zowel DMARC- als BIMI-records bestaan voor een subdomein:

   * DMARC-records kunnen niet worden verwijderd. Als u een BIMI-record wilt verwijderen, moet u eerst de BIMI-record verwijderen.
   * DMARC-records kunnen worden bewerkt, maar de beleidsdowngrade naar Geen is niet toegestaan en de percentagewaarde ervan moet 100 zijn.

