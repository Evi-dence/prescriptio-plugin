---
name: prescriptio-gerer-prospection
description: "Organiser objectifs, cibles, joignabilité, historique, cadence et étapes commerciales dans l'espace Prescriptio, sans lancer implicitement une campagne."
---

# Organiser la prospection

Au début d'une nouvelle séquence, lire `prospection_objectif` sans argument pour connaître l'offre, la cible et l'avancement existants. Un nouvel objectif remplace le précédent ; le modifier seulement si la demande porte sur cet objectif.

`prospection_cibles` lit les cibles de l'espace et pose leur rang. Attention : transmettre un `prospect_id` sans rang retire le rang ; omettre le prospect pour une simple liste. `prospection_profils_cibles` définit les critères propres au compte, sans rédiger de message.

`prospection_coordonnees` avec `action:etat` indique la joignabilité, les exclusions et le domaine, jamais l'adresse ou le numéro. Avec `action:poser`, n'enregistrer que des coordonnées réellement obtenues et leur source. Un repère en `unknown.invalid` n'est pas une adresse utilisable.

Lire `prospection_historique` pour les échanges et prochaines actions avant de proposer une relance. Déposer un échange ou un rendez-vous seulement si l'utilisateur le demande ou si cette synchronisation est déjà autorisée. Ce plugin n'a pas accès à Gmail, Outlook ou à l'agenda par lui-même. Lorsqu'une autre connexion autorisée fournit un événement, conserver son identifiant dans `reference` pour rendre le dépôt idempotent. Une note d'équipe doit contenir les faits utiles, pas tout le fil de conversation.

`prospection_pipeline` lit les étapes et leurs règles. Transmettre `etapes` remplace la configuration entière : préserver les étapes à conserver et expliquer la portée du remplacement. L'appartenance est calculée ; ne pas inventer un déplacement manuel si la règle ne le permet pas.

`prospection_quotidien` lit le bilan ou règle la cadence personnelle. Il ne prépare ni n'envoie de messages. Passer au skill du canal choisi quand la demande devient une préparation de contenu.