# lab5 -Du-Notebook-au-D-ploiement-Conteneuris-d-un-Mod-le-de-Machine-Learning
**Etape 1: Vérifier l’installation de Docker**


Docker a été correctement installé sur la machine et le démon fonctionne.
L’environnement est donc prêt pour la conteneurisation et le déploiement des modèles de Machine Learning.
<img width="821" height="110" alt="image" src="https://github.com/user-attachments/assets/83ca1ab4-1497-4e42-82b6-82ed72da5b4b" />

**Étape 2 : Lancer un serveur Nginx dans un conteneur**


On a lancé avec succès un serveur Nginx dans un conteneur Docker, vérifié son fonctionnement via le navigateur, puis arrêté et supprimé le conteneur, démontrant ainsi la capacité de déployer et gérer des services conteneurisés.


<img width="1260" height="238" alt="image" src="https://github.com/user-attachments/assets/94bd062f-d216-4363-8671-f952848d288f" />
<img width="662" height="235" alt="image" src="https://github.com/user-attachments/assets/c2c22c15-4bf1-4d3e-a7ed-070854a1ba6c" />
<img width="626" height="101" alt="image" src="https://github.com/user-attachments/assets/1f673f3f-b3c0-494d-b1e2-e40ec3afeaa1" />

**Etape 3: Ouvrir un shell Linux isolé dans un conteneur**


On a créé et testé un environnement Linux isolé dans un conteneur Docker.
On a installé des logiciels, démontrant la flexibilité et l’isolation offertes par Docker.
<img width="982" height="461" alt="image" src="https://github.com/user-attachments/assets/220b75a3-c4d3-43f4-94cf-cad40f2a44be" />
<img width="1020" height="92" alt="image" src="https://github.com/user-attachments/assets/4e089164-f8e4-44ff-813b-a8717611487e" />
<img width="671" height="108" alt="image" src="https://github.com/user-attachments/assets/eddf816a-0e22-42e0-a59b-48cdfa657f47" />
<img width="1200" height="131" alt="image" src="https://github.com/user-attachments/assets/f5410abc-9fe3-4471-8bd0-0fe426f8a4e3" />

**Etape 4: Comprendre la structure d’une commande docker run**


On a lancé un conteneur Nginx en arrière-plan sur le port 8081 pour illustrer la structure d’une commande docker run et tester l’accès à un service isolé via Docker.
<img width="814" height="60" alt="image" src="https://github.com/user-attachments/assets/dc6d6edd-19b3-4285-af03-a4f4a890dbc4" />
<img width="1217" height="115" alt="image" src="https://github.com/user-attachments/assets/0ac09651-0d33-4632-b5f3-00d41e3c94d8" />
<img width="575" height="109" alt="image" src="https://github.com/user-attachments/assets/238ba61a-91b9-412e-9125-9c5b182ada87" />


**Etape 5: Conteneuriser l’API churn du projet mlops-lab-01**


<img width="648" height="41" alt="image" src="https://github.com/user-attachments/assets/3e63fcd8-f671-4f8e-b514-d36be3331906" />

**Etape 6: Créer un fichier requirements.txt pour l’image Docker**


Création de requirements.txt
<img width="277" height="200" alt="image" src="https://github.com/user-attachments/assets/f36cd53d-214b-4af4-86a7-a13e86ecbabc" />


**Etape 7: Créer un Dockerfile pour l’API churn**


On a créé un Dockerfile qui permet de construire une image Docker pour l’API churn.
<img width="844" height="494" alt="image" src="https://github.com/user-attachments/assets/f6332b2b-f4a1-4fa0-b44a-32c1e6772b0c" />

**Étape 8 :Préparer un modèle actif avant de construire l’image**


On a vérifié que le dossier models/ contient bien un modèle entraîné et que registry/current_model.txt référence correctement ce modèle actif
<img width="1018" height="144" alt="image" src="https://github.com/user-attachments/assets/6d7e4c95-9004-490b-ba5b-4f3b1a0aff7a" />
<img width="558" height="67" alt="image" src="https://github.com/user-attachments/assets/93802709-9d6f-4fff-b722-9ea883ddcc51" />

**Étape 9 : Construire l’image Docker du projet churn**


On a construit avec succès l’image Docker de l’API churn. Elle est maintenant listée parmi les images locales avec le nom churn-api:latest et un ID unique. Cette image contient tout le projet et ses dépendances, prête à être déployée dans un conteneur.
<img width="801" height="170" alt="image" src="https://github.com/user-attachments/assets/0f351c51-eb41-4c99-996b-78884a4cd5f0" />
<img width="811" height="155" alt="image" src="https://github.com/user-attachments/assets/166879c6-0162-48c8-bbc2-5321cc9909f2" />

**Étape 10 : Lancer l’API churn dans un conteneur**


On a lancé l’API churn dans un conteneur Docker isolé nommé churn-api-demo. Le port 8000 du conteneur est mappé sur le port 8000 de l’hôte, ce qui permet d’accéder à l’API depuis notre navigateur ou via un client HTTP comme curl.
<img width="831" height="252" alt="image" src="https://github.com/user-attachments/assets/c6e056ac-5839-4570-924a-6ee274fb084a" />

Nous avons testé le endpoint /health qui a renvoyé un statut ok et le modèle actif (churn_model_v1_20251227_123807.joblib), confirmant que l’API est opérationnelle et prête à recevoir des requêtes pour prédiction.
<img width="799" height="554" alt="image" src="https://github.com/user-attachments/assets/93442400-45d6-4233-932e-d77df40fb149" />

**Étape 11 : Vérifier les logs générés à l’intérieur du conteneur**


On a lancé le conteneur de l’API churn et vérifié que celui-ci génère bien des logs d’activité et de prédictions à l’intérieur.
<img width="1255" height="245" alt="image" src="https://github.com/user-attachments/assets/33c5d204-5f00-4683-bc68-74b8809cc066" />
<img width="1263" height="71" alt="image" src="https://github.com/user-attachments/assets/9be63503-1f01-4ea8-875a-4d2336d28198" />
<img width="713" height="104" alt="image" src="https://github.com/user-attachments/assets/8c9e8a84-fcc4-4280-8044-1f430b03dbf0" />


**Étape 12 : Orchestration locale avec Docker Compose**


On crée ici un fichier docker-compose.yml pour orchestrer le conteneur de l’API churn. Cela permet de lancer facilement le service avec une seule commande
<img width="766" height="455" alt="image" src="https://github.com/user-attachments/assets/84a2c79a-23d7-493b-a25a-64fad842a55a" />


**Étape 13 : Démarrer l’API via Docker Compose**

on utilise Docker Compose pour lancer l’API churn. L’objectif est de démarrer le conteneur avec toutes ses configurations définies dans docker-compose.yml, sans avoir à retaper la commande docker run.
<img width="1227" height="278" alt="image" src="https://github.com/user-attachments/assets/4cff2d4e-e61b-4179-aaca-c111de1fb792" />
**On teste**
<img width="649" height="24" alt="image" src="https://github.com/user-attachments/assets/3e7a89cc-533a-4a21-999e-293465a21499" />
<img width="898" height="35" alt="image" src="https://github.com/user-attachments/assets/770ad8ea-f258-468f-9189-bfadc7359544" />


**Étape 14 : lancer les services en arrière-plan et observer les logs**


on lance l’API churn en mode détaché avec Docker Compose afin qu’elle s’exécute en arrière-plan. 
<img width="1221" height="444" alt="image" src="https://github.com/user-attachments/assets/0979fbde-6043-4288-a9de-cb55955305c2" />

Les logs sont ensuite consultés en temps réel pour vérifier le bon fonctionnement du service lors des requêtes /health et /predict
<img width="1081" height="153" alt="image" src="https://github.com/user-attachments/assets/a8a85e8f-89eb-4a6d-9b16-990ee25c04c6" />

Puis les services sont arrêtés proprement
<img width="1222" height="163" alt="image" src="https://github.com/user-attachments/assets/af974573-b535-4529-8943-431bcfb50dc1" />


**Étape 15 : lier Docker Compose au reste du cours (Git + DVC)**


on a lié Git, DVC et Docker Compose afin d’obtenir un workflow MLOps local complet. Le code et la configuration sont versionnés avec Git, les données et modèles sont gérés avec DVC, et l’API est déployée de manière reproductible grâce à Docker et Docker Compose.
<img width="1189" height="179" alt="image" src="https://github.com/user-attachments/assets/63857d44-2890-4d5a-8c9c-7ad07cbb76d6" />

