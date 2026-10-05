---
name: prescriptio-repondre-marches
description: "Qualifier un dossier de marché dans Prescriptio, enregistrer une analyse sourcée et préparer livrables, planning, documents et mémoire technique."
---

# Travailler une réponse à un marché

Lire `marches_dossiers` pour retrouver les dossiers de l'organisation et leur `draft_id`. Si l'utilisateur demande de suivre un nouveau marché, `marches_dossier_suivre` reprend son identifiant réel ; il renvoie le dossier existant s'il est déjà suivi.

Lire les pièces pertinentes avec `marches_dce` avant d'enregistrer une analyse. `marches_dossier_analyse_enregistrer` attend un verdict `go`, `no_go` ou `a_verifier`, ses motifs et des références précises. Chaque fait du règlement doit reprendre la pièce, l'emplacement et un extrait exact : le serveur contrôle l'extrait. Ne pas prétendre avoir vérifié une pièce inaccessible. Un nouvel enregistrement remplace l'analyse personnelle précédente ; relire celle-ci pour préserver le travail demandé.

Construire les éléments de réponse à partir du dossier :
- `marches_dossier_livrables` pour les pièces à remettre et leur avancement.
- `marches_dossier_planning` pour les tâches et réunions ; reprendre l'échéance officielle et expliciter le fuseau des heures.
- `marches_dossier_documents` pour l'inventaire et le rattachement de documents existants.
- `marches_bibliotheque` pour les références, CV et extraits privés réellement disponibles.
- `marches_dossier_memoire` pour lire puis écrire les sections demandées. Une écriture remplace la section de même clé.
- `marches_dossier_suivi_modifier` pour les changements de statut et les résultats réellement connus.

Ne pas inventer qualification, référence client, engagement technique, effectif ou prix pour remplir une section. Signaler les informations à obtenir. La préparation et l'enregistrement dans Prescriptio ne déposent pas une offre auprès de l'acheteur.

Après un délai dépassé sur une mutation, relire le dossier avant de rejouer. Restituer les changements effectivement confirmés et les pièces encore manquantes.