pipeline {
  agent {
    docker { image 'install' }   
  }
  stages {
    stage('Install dependencies') {
      steps {
        sh 'npm ci || npm install'
      }
    }
    stage('Run tests') {
      steps {
        sh 'npm test'
      }
    }
  }
  post {
    success { echo 'Tous les tests sont passés !' }
    failure { echo 'Des tests ont échoué.' }
  }
}
