---
name: prescriptio-explorer-reseau
description: "Examiner les relations documentées entre organisations dans Prescriptio, explorer des intermédiaires et analyser le réseau des entreprises suivies."
---

# Examiner un réseau d'organisations

Résoudre les entreprises par SIREN avant d'explorer leurs liens. `reseau_relations_lister` donne les voisins directs d'une entreprise ; conserver les filtres et le décalage pour paginer.

Lire `reseau_relation_preuves_lire` pour chaque paire importante. Distinguer contrat documenté, projet partagé, gouvernance et simple co-mention. Des dirigeants communs, une mention dans un PV ou un post ne prouvent pas une collaboration.

`reseau_chemins_rechercher` explore des chemins limités à trois liens. Relire les preuves de chaque paire avant d'interpréter un chemin. Celui-ci ne prouve ni relation entre les extrémités ni possibilité d'introduction. `reseau_documents_rechercher` approfondit les documents autour d'une organisation.

Lire `coverage` : sources lues, vides ou en erreur, plafonds et troncature. Une recherche vide signifie « non établi dans les sources couvertes ». Les totaux de voisins directs et les chemins indirects n'ont pas le même périmètre. L'index consulté ne correspond pas à une collecte instantanée.

Pour une analyse du réseau privé, `reseau_analyse` avec `action:preparer` et `assistant:claude` fournit le contexte du compte et `analyse_id`. Approfondir les pistes pertinentes puis, si l'utilisateur demande d'enregistrer l'analyse, appeler `action:publier` avec cet identifiant. La synthèse enregistrée est en français, sans HTML ni Markdown, au plus 6 000 caractères, et conserve les URL complètes des sources utiles.