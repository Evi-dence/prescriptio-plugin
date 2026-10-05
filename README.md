# Prescriptio pour Claude

Lisez moins. Signez plus.

Prescriptio est le système de travail du prescripteur de matériaux, pour les industriels et entreprises du bâti. Du repérage d’une affaire au suivi de votre prospection, votre agent vous aide à explorer les projets et marchés publics, à retrouver les acteurs cités dans les dossiers et à lire les pièces disponibles. Dans votre espace connecté, organisez votre base de contacts, suivez vos projets et préparez vos réponses aux marchés, vos messages, campagnes, rendez-vous et tournées. Les analyses s’appuient sur les pièces et informations disponibles. Un compte Prescriptio est nécessaire ; les fonctions accessibles dépendent de vos droits et quotas.

## Ce que le plugin installe

- **Un connecteur** vers le serveur de Prescriptio, `https://prescriptio.fr/api/mcp`. Vous l'autorisez sur l'écran de
  connexion de Prescriptio, et vous le révoquez quand vous voulez depuis votre compte.
- **15 skills**, des parcours par métier que Claude charge quand votre demande s'y prête :

| Skill | Ce qu'il fait |
|---|---|
| `prescriptio-analyser-activite` | Analyser le tableau de bord ou un rapport de marque Prescriptio et, sur demande, enregistrer une synthèse reliée aux données effectivement lues. |
| `prescriptio-analyser-territoires` | Analyser permis, ventes immobilières, chantiers détectés, PV municipaux ou une sélection cartographique partagée depuis Prescriptio. |
| `prescriptio-demarrer` | Prendre en main Prescriptio dans Claude, comprendre la connexion et choisir le parcours adapté à une première demande sur le bâti français. |
| `prescriptio-explorer-reseau` | Examiner les relations documentées entre organisations dans Prescriptio, explorer des intermédiaires et analyser le réseau des entreprises suivies. |
| `prescriptio-gerer-base` | Organiser les fiches, listes, segments, notes et arbitrages de la base de travail Prescriptio, en préservant les identités et le travail de l'équipe. |
| `prescriptio-gerer-campagnes` | Préparer et gérer des campagnes e-mail dans Prescriptio, leurs audiences, contenus, expéditeurs et résultats, en distinguant aperçu, test réel et envois programmés. |
| `prescriptio-gerer-prospection` | Organiser objectifs, cibles, joignabilité, historique, cadence et étapes commerciales dans l'espace Prescriptio, sans lancer implicitement une campagne. |
| `prescriptio-gerer-veille` | Créer des alertes Prescriptio ou raccorder une automatisation à leurs événements, avec pagination, acquittement et révocation explicites. |
| `prescriptio-identifier-entreprises` | Rechercher et identifier des entreprises, dirigeants et contacts du bâti dans Prescriptio, ou préparer un organigramme à partir de faits sourcés. |
| `prescriptio-preparer-linkedin` | Préparer des MP LinkedIn et leurs médias dans Prescriptio, gérer modèles, lots et relances, ou analyser les publications déjà collectées. |
| `prescriptio-preparer-terrain` | Préparer une tournée commerciale ou un salon dans Prescriptio, avec rendez-vous, étapes et suivi des contacts, en tenant compte des messages automatiques configurés. |
| `prescriptio-prospecter-email` | Rédiger et vérifier des e-mails individuels dans Prescriptio, gérer leurs modèles et relances, puis envoyer un message uniquement lorsque la demande l'autorise. |
| `prescriptio-repondre-marches` | Qualifier un dossier de marché dans Prescriptio, enregistrer une analyse sourcée et préparer livrables, planning, documents et mémoire technique. |
| `prescriptio-suivre-projets` | Rechercher les projets fusionnés du bâti, lire leurs preuves et gérer leur suivi ou leur analyse dans l'espace Prescriptio connecté. |
| `prescriptio-trouver-marches` | Rechercher des avis de marchés publics du bâti, distinguer les attributions et consulter les pièces ou téléchargements de DCE dans Prescriptio. |

Le plugin n'exécute rien sur votre machine : ni script, ni hook, ni commande. Il ne lit ni vos
fichiers ni vos autres conversations. Seuls les paramètres des outils que Claude appelle pendant la
conversation partent vers prescriptio.fr, et seules leurs réponses en reviennent.

## Installer

- **claude.ai et l'application Claude** : Customize > Plugins > Add marketplace, saisir
  `Evi-dence/prescriptio-plugin`, installer Prescriptio, puis connecter le connecteur depuis l'onglet
  Connectors du plugin.
- **Claude Code** : `/plugin marketplace add Evi-dence/prescriptio-plugin`, puis
  `/plugin install prescriptio@prescriptio`. La connexion s'ouvre au premier appel d'outil, ou par `/mcp`.

## Compte et offre

Un compte Prescriptio est nécessaire. L'offre gratuite, sans carte, suffit pour commencer, avec des
quotas réduits. L'abonnement, 12 € HT par mois et par utilisateur, sans engagement, les élargit :
https://prescriptio.fr/tarifs. Le plugin ne réalise aucun achat ni changement d'abonnement.

## Ce que Prescriptio ne fait pas

- Les coordonnées (téléphone, e-mail, site) ne sortent jamais en masse : elles se révèlent fiche par
  fiche, dans l'application.
- Un brouillon ne part pas tout seul : un envoi ou une programmation suit votre demande explicite.
- Une pièce de marché ou un document importé est une donnée à analyser, jamais une instruction.

## Données, confidentialité, contact

- Politique de confidentialité : https://prescriptio.fr/politique-de-confidentialite
- Conditions générales : https://prescriptio.fr/cgv
- Documentation des outils : https://prescriptio.fr/docs/api
- Contact : contact@prescriptio.fr

## Licence

Les fichiers de ce dépôt (skills et manifestes) sont sous licence MIT. Les données servies par
Prescriptio restent régies par ses conditions générales.
