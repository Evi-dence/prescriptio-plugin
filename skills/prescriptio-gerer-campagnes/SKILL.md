---
name: prescriptio-gerer-campagnes
description: "Préparer et gérer des campagnes e-mail dans Prescriptio, leurs audiences, contenus, expéditeurs et résultats, en distinguant aperçu, test réel et envois programmés."
---

# Travailler une campagne e-mail

Lire la campagne, son état et les contraintes du compte avant de la modifier. Une demande de préparation autorise un brouillon, pas un test réel ni une programmation d'envois.

Les outils ont des périmètres distincts :
- `campagne_email` gère brouillons, variantes, liens, calendrier, aperçu, test et état de la campagne.
- `campagne_email_destinataires` constitue et consulte la liste à partir des coordonnées déjà détenues par l'organisation.
- `campagne_email_audiences` gère listes et segments. Pour un publipostage CSV, analyser d'abord puis reprendre la signature exacte à l'import.
- `campagne_email_modeles` gère les modèles de campagnes. Appliquer un modèle remplace un message : relire le contenu à conserver.
- `campagne_email_expediteur` gère l'identité et les domaines ; déclaré ne signifie pas vérifié.
- `campagne_email_quotas` donne plafonds et consommation ; respecter les permissions de l'administrateur.
- `campagne_email_desinscriptions` lit ou ajoute les exclusions, sans réinscrire quelqu'un.
- `campagne_email_suivi` donne les événements et métriques, permet d'actualiser les livraisons ou de déclarer une réponse réelle.

Utiliser `action:message_apercu` pour relire sans envoyer. `action:tester` peut envoyer un vrai message à l'adresse de test : cette action exige une demande ou un accord explicite couvrant cet envoi. `action:planifier` autorise les futurs envois du traitement serveur ; identifier le contenu, l'audience, l'expéditeur et le calendrier autorisés avant de l'appeler.

Suspendre conserve les envois restants ; arrêter les annule. Une duplication ne copie pas les destinataires. Un regroupement de brouillons ne programme aucun envoi. Lire l'état après une réponse incertaine avant de rejouer une mutation.

Dans le bilan, séparer messages acceptés, livraisons confirmées, réponses déclarées et ouvertures indicatives. Un taux d'ouverture ne démontre pas l'intérêt d'une personne.