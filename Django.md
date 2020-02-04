# Django
## Démarrer un projet
Créer le répertoire 
Installer un environement virtuel 

`python3 -m venv env-virtuel`ou 

<pre>virtualenv -p python3 venv</pre>


Démarrer l'environnement virtuel
`source env-virtuel/bin/activate`
Installer Django 
`pip install Django`
Créeer le projet
`django-admin startproject mysite`
Démarrer le serveur

`python3 manage.py runserver
Créér une application
python manage.py startapp [MonApp

## Création dépôt git
créer le dépôt sur Github
puis dans le répertoire du projet saisir
echo "# outils_scoop" >> README.md
 1064  git init
 1065  git add README.md 
 1066  git add .gitignore 
 1067  git add outil_scoop/
 1068  git commit -m "first commit"
 1069  git remote add origin https://github.com/louxfaure/outils_scoop.git
 1070  git push -u origin master
 1071  history


