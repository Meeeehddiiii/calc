pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Meeeehddiiii/calc'
            }
        }

        stage('Setup') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest tests/'
            }
        }
    }
}
