# Documentation fonctionnelle 

## Table des matières
* Présentation
	* Défi DIG : concevoir une plateforme numérique dédiée aux parents d’élèves en situation de handicap et/ou à besoins éducatifs particuliers.
	* La problématique
	* L’ambition
	* Le contexte
	* Le produit
* Principales fonctionnalités
	* Pour les usagers
	* Pour les agents


## Présentation
### Défi DIG : concevoir une plateforme numérique dédiée aux parents d’élèves en situation de handicap et/ou à besoins éducatifs particuliers.
- [voir le brief du projet](https://github.com/sofiaboulaarab/Interlocuteur-unique/blob/master/Brief_projet_DIG.md)
- [voir la présentation de la réunion de cadrage](https://github.com/sofiaboulaarab/Interlocuteur-unique/blob/master/20190910%20-%20Re%CC%81union%20de%20cadrage.pdf)
- [voir la présentation du projet à 1 mois de la fin du défi](https://github.com/sofiaboulaarab/Interlocuteur-unique/blob/master/20191114%20-%20Pre%CC%81sentation%20du%20projet.pdf)

### La problématique
Aujourd’hui, les informations sur la scolarisation des élèves en situation de handicap et/ou à besoins éducatifs particuliers sont bien souvent insuffisantes, difficile à trouver et à comprendre pour les parents.
*“C’est le parent qui doit déclencher la prise d’information sans savoir où, comment, auprès de qui, quels sont les droits, quelles sont les possibilités…”* François, parent d’une élève de 7 ans multi-dys.


### L’ambition
Rendre accessibles les informations sur la scolarisation des élèves en situation de handicap et/ou à besoins éducatifs particuliers pour qu’elles soient :
- Lisibles : clarté du vocabulaire, effort de langage et de synthèse
- Compréhensibles : donner la bonne information au bon moment
- Actionnables : l’usager peut agir en fonction de sa situation (contacter un interlocuteur, effectuer une démarche)


### Le contexte
Cette plateforme numérique est la dernière brique du service “Interlocuteur unique” composé d’un numéro unique et d’un formulaire de contact et expérimenté depuis 2018 à l’Académie de Clermont-Ferrand. Il a pour objectif de simplifier l’accès à l’information aux usagers du territoire.

**Elle doit donc être conçue pour être scalable et reproductible.**


### Le produit
Développé par le rectorat de Clermont-Ferrand, le service “vers une école pour tous” est le produit d’une étroite collaboration avec la DMAG et la DINSIC. L’expression de besoin des usages et des agents est exprimée de la façon suivante :

Les usagers ont besoin
- de contacter l’administration par téléphone - numéro unique - fonctionnel depuis 2018
- de contacter l’administration par mail ou formulaire - mail unique - fonctionnel depuis 2018
- de consulter les questions / réponses les plus fréquemment posées - défi DIG en cours de développement
- d’être accompagner dans les démarches administratives - défi DIG en cours de développement
- de trouver le bon interlocuteur pour les accompagner dans leur parcours

Les agents ont besoin
- d’un outil de type “ticketing” pour :
	- traiter les demandes des usagers et répondre rapidement - fonctionnel depuis 2018
	- tracer les demandes et effectuer des statistiques - fonctionnel depuis 2018
- d’un service web pour :
	- constituer une base de connaissance et la mettre à disposition des usagers - défi DIG en cours de développement


## Principales fonctionnalités
### Usagers
**Page d’accueil**
- Naviguer dans le site
- Accéder aux différents contenus via des raccourcis

**Questions / Réponses**
- Accéder aux catégories de questions / réponses (ancre)
- Visualiser les réponses aux questions
- Voter la pertinence d’une réponse

**Guide démarches**
- Sélectionner une démarche en fonction de sa situation
- Afficher les coordonnées des interlocuteurs
- Sélectionner son établissement (pour afficher les coordonnées)
- Modifier le choix de l’établissement (pour afficher de nouvelles coordonnées)
- *demain* faire la démarche en ligne

**Interlocuteurs**
- Afficher les coordonnées des interlocuteurs
- Sélectionner son établissement (pour afficher les coordonnées)
- Modifier le choix de l’établissement (pour afficher de nouvelles coordonnées)

**Contact**
- Sélectionner son département
- Renseigner son nom, prénom, objet de la demande
- Rédiger la demande
- Ajouter des pièces-jointes (2 maximum)
- Modifier / supprimer les pièces-jointes
- Envoyer la demande
- Recevoir une confirmation de l’envoi (après l’envoi du formulaire)
- Recevoir un message sur sa boite mail confirmant la prise en charge de la demande par un agent (une fois un agent rendu propriétaire de la demande)


### Agent
**Contenus**
- L’agent peut créer / modifier / supprimer une catégorie de Questions / Réponses
- L’agent peut créer / modifier / supprimer une Question / Réponse
- L’agent peut créer / modifier / supprimer une catégorie de Guide démarche
- L’agent peut créer / modifier / supprimer un Guide démarche
- L’agent peut créer / modifier / supprimer une catégorie d’Interlocuteurs
- L’agent peut créer / modifier / supprimer un Interlocuteur

**Traitement des demandes**
- L’agent reçoit une alerte mail à chaque nouvelle demande reçue. Cette alerte contient les pièces-jointes et un lien vers la demande.
- Le lien vers la demande permet d’accéder (après identification) au détail de la demande sur l’outil de ticketing dédié (à Clermont : OTRS)
- L’agent se rend propriétaire du ticket ce qui génère l’envoi du message la boite mail de l’usager confirmant la prise en charge de la demande par un agent
- Le ticket est considéré comme ouvert
	- ou la demande est de 1er niveau et l’agent répond immédiatement
	- ou la demande est transféré à de l’agent à un agent expert par mail
		- l’agent expert répond directement au demandeur par mail (limite d’OTRS : dans ce cas là on perd la traçabilité de la demande, ce qui complexifie la fermeture du ticket et perturbe les statistiques de temps de traitement des demandes)
		- l’agent expert communique la réponse à l’agent qui répond au demandeur (limite : workflow peu fluide)
- Le ticket peut être fermé à tout moment par l’agent qui peut également à ce moment là déclencher une enquête de satisfaction
- L’agent peut exporter les statistiques des demandes (statut, traitement, etc.)
- L’agent peut exporter les contenus -> pas par OTRS - BO  application 
- L’agent peut attribuer une demande à un autre agent en modifiant le propriétaire
- L’agent peut attribuer une demande à une file spécifique


### Admin
**OTRS**
- L’administrateur peut créer des files de traitement
- L’administrateur peut créer des propriétaireq
- L’administrateur peut créer les règles pour l’affichage des statistiques

**Service en ligne**
- ???
