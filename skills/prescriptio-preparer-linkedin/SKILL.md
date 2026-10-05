---
name: prescriptio-preparer-linkedin
description: "Préparer des MP LinkedIn et leurs médias dans Prescriptio, gérer modèles, lots et relances, ou analyser les publications déjà collectées."
---

# Préparer le travail LinkedIn

Pour une nouvelle séquence de prospection, lire l'objectif existant et l'historique pertinent avant d'écrire. `linkedin_prospects` fournit les profils disponibles, les éléments publics collectés et les relances dues. Ne pas transformer un ancien titre en fonction actuelle vérifiée.

Si un profil doit être rattaché, utiliser `linkedin_profil_rattacher` avec l'URL connue. `linkedin_profil_actualisation` dépose une demande à l'extension ; il ne lit pas immédiatement LinkedIn. Une demande peut attendre une validation ou expirer. Relire `action:etat`, puis le prospect ; annoncer uniquement l'état retourné.

Pour écrire avec la voix de l'utilisateur, lire `linkedin_publications_rechercher` avec `scope:mine`. Examiner disponibilité et troncature du texte. `scope:shared` fournit des exemples d'autres auteurs, pas la voix de l'utilisateur. `linkedin_publications_statistiques` mesure les publications collectées ; présenter les commentaires avec impressions et réactions, sans prétendre que ces chiffres décrivent tous les posts existants.

Préparer le message demandé :
- `linkedin_modeles` lit les modèles du compte et leurs captures, sans imposer un texte ou un nombre d'images commun à tous.
- `linkedin_mp_preparer` reprend le modèle et sa révision ; seules les parties personnalisables changent.
- `linkedin_mp_brouillon_enregistrer` convient à un brouillon libre déjà rédigé.
- `linkedin_mp_media_ajouter` ajoute les médias demandés ; ne pas remplacer implicitement les captures obligatoires.
- `linkedin_mp_verifier` distingue les fichiers présents sur le serveur de la préparation confirmée par l'extension.

`linkedin_mp_lots` organise plusieurs messages ; la validation nécessite l'accord de l'utilisateur et n'envoie rien. `linkedin_mp_planning` fixe une échéance en heure de Paris, pas un envoi automatique. `linkedin_mp_statut` et `linkedin_relances` peuvent déclarer une touche déjà partie : ne le faire qu'avec une preuve ou une déclaration de l'utilisateur. Ces outils ne cliquent pas sur Envoyer dans LinkedIn.