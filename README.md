# Java-RMI-gRPC-Sockets
## Application TaskList avec Java RMI

Ce dépôt contient une application TaskList qui utilise Java RMI pour gérer une liste de tâches.

### Déploiement

#### Prérequis
- Java Development Kit (JDK) installé
- Git installé
- Un environnement de développement Java compatible avec RMI (par exemple, Eclipse, IntelliJ IDEA)

#### Étapes de déploiement

1. Clonez le dépôt sur votre machine
   
2. Ouvrez le projet dans votre environnement de développement Java.

3. Compilez le code source pour générer les fichiers .class.

4. Démarrez le serveur RMI en exécutant la classe `TaskListServer`. Assurez-vous que le registre RMI est accessible sur le port 1099.

5. Démarrez le client RMI en exécutant la classe `TaskListClient`. Assurez-vous que le client se connecte au serveur RMI correctement.

### Test de l'application

Une fois l'application déployée, vous pouvez tester son fonctionnement en ajoutant, supprimant et récupérant des tâches à partir du serveur.

Voici quelques exemples de commandes pour tester l'application :

- Ajouter une tâche :

taskList.addTask("Faire les courses");


- Supprimer une tâche :
taskList.removeTask("Faire les courses");


- Récupérer toutes les tâches :
List<String> allTasks = taskList.getAllTasks();

Assurez-vous de vérifier la console pour voir les résultats des opérations effectuées.

## Application Messaging Service avec gRPC

### Déploiement
Assurez-vous d'avoir Java JDK 8 ou supérieur installé sur votre système.
Clonez le dépôt sur votre machine locale.
Accédez au répertoire du projet.
Compilez les fichiers source.
### Test de l'application
#### Démarrage du serveur
Exécutez le serveur gRPC en utilisant la classe MessageServer.
Le serveur démarrera sur le port 8080 et sera prêt à recevoir des messages.
#### Envoi de messages
Exécutez le client d'envoi de messages en utilisant la classe SendMessageClient.
Suivez les instructions pour saisir les informations nécessaires telles que l'identifiant de l'expéditeur, l'identifiant du destinataire et le texte du message.
#### Récupération des messages
Exécutez le client de récupération de messages en utilisant la classe GetMessagesClient.
Entrez l'identifiant de l'utilisateur pour lequel vous souhaitez récupérer les messages.

## Chat Application
### Installation
Assurez-vous d'avoir Java JDK installé sur votre système.
Téléchargez les fichiers source de l'application depuis le dépôt GitHub.

### Configuration
Ouvrez le fichier ChatServer.java et modifiez si nécessaire le numéro de port utilisé par le serveur (par défaut : 12345).
Compilez le code en exécutant la commande javac ChatServer.java dans le répertoire contenant le fichier.
Faites de même pour les fichiers ChatClient1.java et ChatClient2.java.
### Déploiement du Serveur
Démarrez le serveur en exécutant la commande java ChatServer dans le répertoire contenant le fichier compilé ChatServer.class.
Le serveur de chat devrait démarrer et afficher un message indiquant qu'il écoute sur le port spécifié.
### Utilisation des Clients
Pour démarrer un client de chat, exécutez la commande java ChatClient1 ou java ChatClient2 dans des terminaux différents ou dans des fenêtres de terminal distinctes.
Les clients se connecteront automatiquement au serveur en utilisant l'adresse IP 127.0.0.1 et le port spécifié.
Vous pouvez maintenant envoyer des messages depuis les clients et les voir apparaître sur les autres clients connectés au serveur.

### Tests
Connectez plusieurs clients au serveur et vérifiez que les messages sont bien transmis à tous les clients.
Déconnectez un client et vérifiez que les autres clients continuent à fonctionner correctement.

