
# =============INSTALLATION DU PROJET===================

#     ----- Structure du projet-------
 
tp_bi(v3)/
├── Front/
│   ├── css/
│   │   ├── home.css
│   │   └── style.css
│   ├── images/
│   │   ├── photo-1498887960847-2a5e46312788.avif
│   │   └── user.svg
│   ├── my-playwright-project/
│   │   ├── node_modules/
│   │   ├── test/
│   │   │   ├── home.spec.js
│   │   │   ├── login.spec.js
│   │   │   └── register.spec.js
│   │   ├── test-results/
│   │   ├── package-lock.json
│   │   ├── package.json
│   │   └── playwright.config.js
│   ├── script/
│   │   └── home.js
│   ├── home.html
│   ├── login.html
│   ├── register.html
│   └── middlewares/
├── node_modules/
├── src/
│   ├── Configs/
│   │   └── databases.js
│   ├── Controllers/
│   │   ├── vehicleController.js
│   │   └── userController.js
│   ├── Models/
│   │   ├── vehicle.js
│   │   └── user.js
│   ├── Routes/
│   │   ├── vehicleRoutes.js
│   │   └── userRoutes.js
│   ├── seeders/
│   │   ├── userSeeder.js
│   │   └── vehicleSeeder.js
│   ├── middlewares/
│   │   └── authMiddleware.js
│   ├── app.js
│   └── serveur.js
├── Test/
│   ├── vehicle.test.js
│   └── user.test.js
├── .env
├── docker-compose.yml
└── package.json

Avant tous faut prealable :

# Cloner le dépôt et naviguer vers le répertoire du projet
	git clone <URL_DE_VOTRE_DEPOT>
	cd tp_bi(v3) # Naviguez vers le dossier racine du projet
#  ============INSTALLATION DES DEPENDANCES BACKEND ET TEST===================
 
1. Stack Technologique
----------------------

- Node.js : environnement JavaScript serveur.
- Express.js : framework REST.
- Sequelize : ORM SQL.
- MySQL : base de données.
- Docker : conteneurisation.
- Jest : tests.
- Postman : tests manuels.
- Nodemon : actualisation automatique du serveur.
- Dotenv : externalisation des variables d’environnement .
- React : future interface utilisateur.


2. Initialisation du Projet
---------------------------
Prérequis:
	- installer : docker et nodejs en global.
 
* initialisation des packages :
   Ce placer a la racine  du projet ou est present le package.json
 	~: npm init -y
 	~: npm install express sequelize mysql2 dotenv jsonwebtoken bcrypt cors cookie-parser
 	~: npm install --save-dev nodemon jest sequelize-cli


* lancement de la bd virtuelle (docker mysql) :
	ps : toujours vérifier la présence du docker-compose.yml  à la racine du projet.
  	~: sudo docker compose up -d 
  	
  3. Lancer le serveur
--------------------
Prérequis:
- avoir lancer son docker mysql

 	~: npm run dev
 	
4. Tester avec Jest
-------------------
Prérequis:
- avoir lancer son docker mysql

	~:npm run test:backend


# ============INSTALLATION DES DEPENDANCES FRONTEND ET TEST===================
 
 1. Installer les dépendances spécifiques à Playwright (Frontend)
 
   ~cd Front/my-playwright-project/
   ~npm init -y
   ~npm install --save-dev @playwright/test
   ~npx playwright install
   
 2. Lancer les Test
  
   ~npx playwright test test/
   
 3. Test avec affichage dans le navigateur
 
   ~npx playwright test test/ --headed
   
   Pour lancer les test frontend de chaque fichier il faudra juste specifier les fichier
   
   exemple : ~npx playwright test test/ login.spec.js --headed

Dans mes codes de test j ai mis des commentaire pour expliquer en detaille le but de chaque implementation 



# MERCI MONSIEUR POUR CETTE CONNAISSANCE QUE VOUS NOUS AVEZ APRIS 🙏 
