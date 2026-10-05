---
name: prescriptio-identifier-entreprises
description: "Rechercher et identifier des entreprises, dirigeants et contacts du bâti dans Prescriptio, ou préparer un organigramme à partir de faits sourcés."
---

# Identifier des entreprises et leurs interlocuteurs

Utiliser `annuaire_entreprises` pour une entreprise connue ou une liste par activité et territoire. Réutiliser le SIREN à neuf chiffres ou le SIRET à quatorze chiffres retourné ; un nom seul ne suffit pas à lever une homonymie. Un filtre NAF peut suffire sans requête textuelle. Conserver les filtres lors de la pagination.

`recherche` sert au repérage d'un sujet encore imprécis dans plusieurs sources. Pour des avis ouverts ou une échéance de marché, choisir directement `marches_rechercher`. Dans la recherche générale, une virgule sépare des sujets alternatifs ; plusieurs mots dans un même sujet sont recherchés ensemble.

Approfondir selon le besoin :
- `annuaire_dirigeants` : mandats et représentants légaux connus.
- `annuaire_contacts` : personnes, fonctions et rattachements disponibles.
- `annuaire_annonces_legales` : annonces datées ; une ancienne annonce ne démontre pas à elle seule la situation actuelle.
- `annuaire_organigramme` : préparer les personnes connues, puis organiser ou publier la synthèse demandée dans l'espace connecté.

Pour un organigramme, commencer par `action:preparer` avec `assistant:claude`, conserver `analyse_id` et les clés retournées. Distinguer titre déclaré, mandat légal et niveau décisionnel déduit. Publier seulement les modifications demandées, avec les clés connues ; un titre social ne prouve pas un pouvoir de signature.

Les annuaires ne rendent pas les e-mails et téléphones personnels. Ne pas les deviner ni présenter un domaine comme une adresse vérifiée. Le reveal dans Prescriptio reste distinct de la recherche.

Restituer l'identité, les faits utiles, leurs dates et les liens effectivement obtenus. Un champ absent reste inconnu ; ne pas compléter un bilan ou un effectif à partir d'une estimation non sourcée.