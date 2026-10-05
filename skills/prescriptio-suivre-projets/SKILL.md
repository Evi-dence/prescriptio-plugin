---
name: prescriptio-suivre-projets
description: "Rechercher les projets fusionnés du bâti, lire leurs preuves et gérer leur suivi ou leur analyse dans l'espace Prescriptio connecté."
---

# Rechercher et suivre des projets

`projets_rechercher` reprend `query_string` depuis la sélection Prescriptio, sans le point d'interrogation. Conserver les paramètres répétés des départements, communes, stades, segments, sources ou rôles. `fresh=0` ouvre tout l'historique ; sans précision, la période est de 365 jours. Paginer avec la requête retournée, sans reconstruire les filtres.

Lire `projets_fiche_lire` pour les preuves datées, les acteurs, les rôles, les rapprochements possibles et le suivi de l'organisation. Un rapprochement n'est pas une fusion confirmée ; une étape commerciale n'est pas un avancement du chantier. Distinguer date d'événement et date d'intégration. Une date future ou une attribution ne prouve pas un fait survenu.

Sur demande, `projets_suivi_modifier` suit, archive ou modifie le travail sur le projet. Lire la fiche avant une commande `travail`, car elle remplace plusieurs valeurs. Conserver une clé par intention pour éviter de doubler une note au rejeu. Archiver conserve l'historique et coupe les alertes ; retirer une relation au projet ne retire pas l'entreprise de la base.

Pour une synthèse de secteur, `projets_analyse` avec `action:preparer` et `assistant:claude` fournit le périmètre du compte et `analyse_id`. Vérifier les fiches utiles avant la synthèse. Si l'enregistrement est demandé, `action:publier` reprend cet identifiant, au plus 6 000 caractères sans HTML ni Markdown, avec les URL complètes des sources.