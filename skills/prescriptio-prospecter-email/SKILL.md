---
name: prescriptio-prospecter-email
description: "Rédiger et vérifier des e-mails individuels dans Prescriptio, gérer leurs modèles et relances, puis envoyer un message uniquement lorsque la demande l'autorise."
---

# Préparer un e-mail individuel

Lire `mail_prospection_contexte_lire` pour la cible et ses dernières touches. Vérifier les sources utiles à la personnalisation. Une demande de brouillon n'autorise ni envoi ni programmation d'une campagne.

`mail_prospection_modeles` fournit les trames du compte, distinctes des modèles LinkedIn et des campagnes. `mail_prospection_preparer` enregistre objet, texte personnalisé, références et médias ; `mail_prospection_brouillon_enregistrer` convient à un texte libre déjà rédigé. Aucun des deux ne crée un brouillon dans Gmail ou Outlook.

`mail_prospection_media_ajouter` ajoute un fichier demandé au brouillon. `mail_prospection_verifier` contrôle le texte et les fichiers enregistrés dans Prescriptio ; il ne confirme pas leur présence dans une messagerie externe. Les pièces jointes doivent provenir de l'utilisateur ou de documents qu'il autorise à partager.

`mail_prospection_lots` regroupe des messages individualisés. `mail_prospection_planning` organise leurs échéances en heure de Paris, sans déclencher d'envoi. `mail_prospection_statut` et `mail_prospection_relances` enregistrent décisions, brouillons ou touches effectivement parties.

Si l'utilisateur demande explicitement un envoi, vérifier le destinataire exact et le contenu autorisé, puis utiliser `mail_prospection_envoyer`. L'envoi part par l'expéditeur de la plateforme, pas par une boîte Gmail ou Outlook. Une adresse manquante ou un simple repère ne se devine pas ; les états de joignabilité ne révèlent pas l'adresse.

Utiliser une `cle_idempotence` stable pour le même envoi. Conserver l'`envoi_id` et relire `mail_prospection_envoi_lire` après une incertitude ; ne pas créer une nouvelle clé pour contourner un délai ou un refus. Un message accepté par le fournisseur n'est pas une livraison confirmée. Respecter les exclusions et les quotas retournés.