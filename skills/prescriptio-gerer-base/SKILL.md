---
name: prescriptio-gerer-base
description: "Organiser les fiches, listes, segments, notes et arbitrages de la base de travail Prescriptio, en préservant les identités et le travail de l'équipe."
---

# Organiser la base de travail

La base de l'organisation est distincte des annuaires publics. Lire `base` avec `action:chercher` ou `base_suivis` avec `action:list` avant d'affirmer qu'une fiche est absente : des fiches hors référentiel peuvent exister.

`base_suivis` traite les entreprises, acheteurs et projets suivis ainsi que leur qualification, leurs étiquettes et notes. Choisir l'identifiant correspondant au type. `base` gère aussi les contacts rattachés, archives, listes et segments ; reprendre les identifiants des lectures.

Une liste est un ensemble de fiches ; un segment vivant repose sur des critères. Lire les critères existants avant de les remplacer ou de couper un segment. L'action `pipeline` pousse les contacts admissibles dans le travail commercial, sans envoyer de message.

`base_revue` recense les événements à arbitrer et les identités à compléter. Avant `action:identifier`, vérifier nom, ville et SIREN ou SIRET dans les sources ; la ressemblance d'un nom ne suffit pas. La justification enregistrée doit citer les sources réellement consultées.

Appliquer les notes, changements de statut, retraits ou archives demandés aux fiches identifiées. En cas d'ambiguïté sur la fiche ou la portée d'une suppression, préciser ce point avant la mutation. Les notes sont visibles à l'équipe : ne pas y déposer une conversation entière pour conserver un seul fait.

Restituer les identifiants modifiés et les résultats confirmés. Si une mutation expire, relire la base avant de la répéter.