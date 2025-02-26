pipeline {
    agent any

    stages {

        stage('Setup') {
            steps {
                script {
                    // Créer un environnement virtuel
                    sh 'python3 -m venv venv'  // Crée un environnement virtuel nommé 'venv'

                    // Activer l'environnement virtuel
                    sh '. venv/bin/activate'  // Active l'environnement virtuel

                    // Installer les dépendances avec pip
                    sh 'pip install -r requirements.txt'  // Installe les dépendances dans l'environnement virtuel
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    // Activer l'environnement virtuel et exécuter les tests
                    sh '. venv/bin/activate && pytest tests/'  // Active l'environnement virtuel et lance pytest
                }
            }
        }
    }

    post {
        always {
            // Nettoyage, supprimer l'environnement virtuel après le build
            sh 'rm -rf venv'  // Supprimer l'environnement virtuel pour garder l'espace propre
        }
    }
}
