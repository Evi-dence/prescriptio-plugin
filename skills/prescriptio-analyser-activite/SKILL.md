---
name: prescriptio-analyser-activite
description: "Analyser le tableau de bord ou un rapport de marque Prescriptio et, sur demande, enregistrer une synthèse reliée aux données effectivement lues."
---

# Analyser l'activité ou un rapport de marque

Pour le tableau de bord, `reporting` avec `action:preparer` et `assistant:claude` fournit le contexte personnel et `report_id`. Approfondir uniquement les points utiles à la demande avec les outils disponibles. Séparer faits, interprétations et prochaines actions proposées.

Si l'utilisateur demande d'enregistrer la synthèse dans le tableau de bord, appeler `action:publier` avec le même `report_id`. Le texte enregistré est en français, sans HTML ni Markdown, au plus 6 000 caractères. Une analyse dans la conversation ne nécessite pas à elle seule une publication dans le compte.

Pour une détection de marque, `marque_rapport` avec `action:preparer` et `assistant:claude` lit un rapport figé disponible, ses chiffres et ses renvois numérotés. La lecture ne lance pas une nouvelle collecte. Un refus lié aux droits du compte est une indisponibilité à expliquer, sans proposer un achat dans ce plugin.

Conserver `rapport_id` et les renvois fournis. Chaque phrase de l'analyse de marque enregistrée se termine par au moins un renvoi `[n]` qui l'étaye. Ne pas créer un renvoi pour une idée sans source. `action:publier` enregistre le texte demandé, daté et attribué, dans la page du rapport.

Restituer la période, les limites de couverture et le résultat de l'enregistrement s'il a eu lieu. Des mentions mesurées dans un corpus ne constituent pas une part de marché économique.