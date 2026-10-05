---
name: prescriptio-gerer-veille
description: "Créer des alertes Prescriptio ou raccorder une automatisation à leurs événements, avec pagination, acquittement et révocation explicites."
---

# Organiser une veille

`evenements_alertes` lit, crée et supprime les recherches surveillées du compte. Pour créer une alerte, reprendre sujet, sources, territoire et fréquence demandés. Lire les avertissements : les filtres et la fraîcheur diffèrent selon les sources. La fréquence dite temps réel correspond aux passages du traitement, pas à une ingestion instantanée.

Lister avant de modifier une alerte. Le remplacement passe par suppression et création ; ne pas supprimer une alerte sans identifier précisément celle que l'utilisateur veut remplacer.

Les outils d'événements raccordent une automatisation existante :
- `evenements_abonnement_creer` crée un abonnement aux futurs événements d'une alerte active, avec une clé stable par automatisation.
- `evenements_lire` utilise le `subscription_id` et le `checkpoint` retournés. Le checkpoint signé est distinct des curseurs des autres outils.
- Dédupliquer par identifiant d'événement. La lecture n'acquitte rien ; rejouer une lecture peut rendre les mêmes événements.
- `evenements_acquitter` reprend l'`ack_token` exact après traitement réussi de l'événement concerné.
- `evenements_abonnement_revoquer` coupe les prochaines lectures de cet abonnement.

Créer un abonnement ne crée pas un agent autonome, une tâche planifiée ou un envoi d'e-mail dans Claude. Ne promettre une surveillance future que si une automatisation autorisée a réellement été configurée dans un environnement qui l'exécute. Sinon, expliquer ce que l'alerte Prescriptio fait et ce qui reste à raccorder.

Après un checkpoint expiré ou un refus d'accès, suivre l'erreur ; ne pas inventer un curseur ni un acquittement pour avancer.