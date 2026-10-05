---
name: prescriptio-analyser-territoires
description: "Analyser permis, ventes immobilières, chantiers détectés, PV municipaux ou une sélection cartographique partagée depuis Prescriptio."
---

# Analyser un territoire

Préciser le territoire de la demande et utiliser les filtres adaptés. Un code INSEE n'est pas un code postal. Ne pas transformer une page de résultats en inventaire exhaustif.

`carto_permis_rechercher` filtre les permis par type et état. Une autorisation ne prouve pas l'ouverture du chantier ; une surface absente reste inconnue. `carto_chantiers_rechercher` rend des observations sur image datée : citer la date du relevé, sans présenter la confiance comme une probabilité ni l'observation comme une situation actuelle garantie.

Avec `carto_transactions`, une ligne correspond à une mutation pouvant agréger plusieurs biens. La valeur totale n'est pas le prix de chaque parcelle. Pour un prix moyen, médian ou une comparaison annuelle, utiliser `mode:statistiques` sur une commune ; ne pas calculer une moyenne sur la seule page de ventes reçue. Indiquer la période et la couverture retournées.

Pour une vue confiée par l'utilisateur, `carto_selection_lire` reprend `contexte_id` et sa `revision`. Utiliser les statistiques du serveur ; les points peuvent être plafonnés. Paginer en conservant la collection, le contexte et la révision. Pour enregistrer l'analyse demandée, `carto_analyse_enregistrer` reprend cette révision et une clé stable par intention. Les identifiants cités et les objets prioritaires doivent provenir de la lecture ; au plus 50 objets peuvent être proposés. L'analyse reste dans l'organisation et ne déplace pas la carte.

`mairies_deliberations` recherche les extraits puis relit le PV par `pv_id`, avec pagination. Distinguer discussion, décision votée et mise en œuvre effective. `mairies_pv_lien_obtenir` fournit le PDF disponible ; un lien signé est temporaire. Dans la synthèse, citer commune, date, passage et source utiles.