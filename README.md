# 📚 Gestion Profile

Une application web moderne de **gestion de profils utilisateurs** pour les institutions éducatives (universités, écoles, etc.). Cette plateforme permet une gestion complète des utilisateurs, des cours et des notes avec un système de rôles et de permissions granulaires.

## 🎯 Fonctionnalités

### Pour les Administrateurs
- ✅ Gestion complète des utilisateurs (créer, modifier, supprimer)
- ✅ Assignation des rôles (Admin, Professeur, Étudiant)
- ✅ Visualisation de tous les cours et inscriptions
- ✅ Consultation des notes et performances

### Pour les Professeurs
- ✅ Création et gestion de cours
- ✅ Inscription des étudiants aux cours
- ✅ Saisie et modification des notes
- ✅ Suivi des performances des étudiants
- ✅ Profil personnalisé avec photo

### Pour les Étudiants
- ✅ Consultation des cours inscrits
- ✅ Visualisation des notes reçues
- ✅ Profil personnalisé avec photo et introduction
- ✅ Affichage des professeurs

## 🛠️ Technologies Utilisées

| Technologie | Version | Utilisation |
|-------------|---------|-------------|
| **Python** | 3.x | Backend (logique applicative) |
| **Flask** | - | Framework web Python |
| **Flask-MySQL** | - | ORM pour MySQL |
| **Flask-Login** | - | Gestion de l'authentification |
| **HTML5** | - | Structuration des pages |
| **CSS3** | - | Styling et responsive design |
| **MySQL** | - | Base de données relationnelle |

## 📋 Prérequis

- Python 3.7+
- MySQL Server
- pip (gestionnaire de paquets Python)

## 🚀 Installation

### 1. Cloner le repository
```bash
git clone https://github.com/Mokhtar-46/gestion_profile.git
cd gestion_profile
```

### 2. Créer un environnement virtuel
```bash
python -m venv venv
```

### 3. Activer l'environnement virtuel
- **Sur Windows :**
  ```bash
  venv\Scripts\activate
  ```
- **Sur macOS/Linux :**
  ```bash
  source venv/bin/activate
  ```

### 4. Installer les dépendances
```bash
pip install -r requirements.txt
```

### 5. Configurer la base de données
- Créer une base de données MySQL
- Configurer les paramètres de connexion dans `config.py`

### 6. Lancer l'application
```bash
python app.py
```

L'application sera accessible sur `http://localhost:5000`

## 🗂️ Structure du Projet

```
gestion_profile/
├── app.py                 # Application principale
├── config.py              # Configuration (BD, dossiers, etc.)
├── requirements.txt       # Dépendances Python
├── templates/             # Templates HTML
│   ├── index.html
│   ├── login.html
│   ├── profile.html
│   ├── admin_dashboard.html
│   ├── manage_users.html
│   ├── add_user.html
│   ├── edit_user.html
│   ├── admin_courses.html
│   ├── professor_dashboard.html
│   ├── create_course.html
│   ├── course_detail.html
│   └── student_dashboard.html
├── static/                # Fichiers statiques (CSS, JS)
└── uploads/               # Dossier pour les photos de profil
```

## 🔐 Système de Rôles et Permissions

| Rôle | Accès | Permissions |
|------|-------|-------------|
| **Admin** | Dashboard Admin | Gestion utilisateurs, Visualisation tous les cours |
| **Professeur** | Dashboard Professeur | Création de cours, Gestion des notes |
| **Étudiant** | Dashboard Étudiant | Consultation cours et notes |

## 💾 Schéma Base de Données

La base de données comprend les tables suivantes :

- **user** : Stockage des utilisateurs (id, username, password, email, role, introduction, photo)
- **course** : Gestion des cours (id, name, professor_id)
- **enrollment** : Inscriptions (id, student_id, course_id)
- **grade** : Notes (id, enrollment_id, grade)

## 📷 Fonctionnalités de Profil

- Upload de photo de profil (formats : jpg, png, etc.)
- Introduction personnalisée
- Modification des informations de compte
- Affichage public du profil utilisateur

## 🔒 Sécurité

- ✅ Authentification par login/password
- ✅ Vérification des rôles pour chaque route
- ✅ Redirection automatique vers login si non authentifié
- ✅ Validation des données avec `secure_filename()`

## 📝 Utilisation

### Créer un compte administrateur
1. Accédez à `http://localhost:5000/login`
2. Les premières insertions doivent être faites directement en base de données

### Créer des utilisateurs
1. Connectez-vous en tant qu'administrateur
2. Allez dans **Gestion des utilisateurs**
3. Cliquez sur **Ajouter un utilisateur**
4. Remplissez le formulaire et sélectionnez le rôle

### Créer un cours (Professeur)
1. Connectez-vous en tant que professeur
2. Allez dans **Créer un cours**
3. Remplissez le nom du cours
4. Inscrivez les étudiants depuis la page du cours


---
