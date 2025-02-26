pipeline {
    agent any

    stages {

        stage('Setup') {
            steps {
                sh 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest tests/'
            }
        }
    }
}
