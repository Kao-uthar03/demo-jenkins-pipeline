pipeline {
    agent any

    stages {
        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run tests') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo 'Tous les tests sont passés avec succès !'
        }
        failure {
            echo 'Des tests ont échoué !'
        }
    }
}
