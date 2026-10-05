---
name: prescriptio-preparer-terrain
description: "Préparer une tournée commerciale ou un salon dans Prescriptio, avec rendez-vous, étapes et suivi des contacts, en tenant compte des messages automatiques configurés."
---

# Préparer une tournée ou un salon

Pour une tournée, lire les tournées existantes avec `tournees`. Partir du jour, du départ et des rendez-vous fixes demandés ; ne pas supposer la position actuelle de l'utilisateur.

Créer la tournée puis ajouter les rendez-vous à heure fixe. `action:proposer` recherche les prospects à proximité ; n'ajouter que les étapes pertinentes demandées. Une étape issue du référentiel peut entrer dans la base de travail. `action:optimiser` fournit l'ordre et le trajet ; présenter les horaires comme une préparation, pas une garantie de temps de parcours.

`action:preparer` prépare les messages liés aux étapes. L'outil ne les envoie pas. `action:marquer` constate un état réel ; `action:client` change la qualification commerciale. `action:feuille_de_route` conserve la feuille de route demandée. Ne pas marquer un rendez-vous effectué ou un message envoyé par déduction.

Pour un salon, `salons` avec `action:annuaire` consulte les événements disponibles, leurs dates, la source et la date de vérification. `action:participer` crée le salon de l'organisation et sa préparation, sans acheter de billet.

Avant d'ajouter un contact de salon, lire `action:parametres` : un message automatique peut être envoyé après le délai configuré. L'ajout ne doit pas servir à déclencher cet envoi sans l'autorisation de l'utilisateur. Si la demande porte uniquement sur la conservation d'un contact, préciser l'effet avant l'ajout lorsque l'envoi automatique est actif ; ne pas modifier silencieusement les paramètres de toute l'organisation.

`action:lister` donne les contacts et l'état du suivi sans révéler leur adresse. `action:performances` mesure les résultats disponibles du salon. Les coûts, contacts, messages et avancées commerciales ont des dénominateurs distincts ; garder leur périmètre dans le bilan.