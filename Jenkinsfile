pipeline {
    agent any

    stages {

        stage('Setup') {
            steps {
                // Vérifier si python3 est installé
                sh 'python3 --version'  // Affiche la version de Python 3 pour vérification
                // Installer les dépendances avec pip
                sh 'python3 -m ensurepip --upgrade'  // Assurer que pip est installé et à jour
                sh 'python3 -m pip install -r requirements.txt'  // Installer les dépendances
            }
        }

        stage('Run Tests') {
            steps {
                // Exécuter les tests avec pytest
                sh 'pytest tests/'  // Exécute les tests dans le dossier tests/
            }
        }
    }
}
