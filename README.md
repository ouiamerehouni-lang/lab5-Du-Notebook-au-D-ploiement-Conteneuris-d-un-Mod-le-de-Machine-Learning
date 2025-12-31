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


 
