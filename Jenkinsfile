pipeline {
  agent any
  tools { nodejs 'install' }

  stages {
    stage('Install dependencies') {
      steps {
        sh 'npm ci'
      }
    }
    stage('Run tests') {
      steps {
        sh 'npm test -- --ci'
      }
    }
  }
  post {
    success { echo ' Tests OK' }
    failure { echo ' Échec' }
  }
}
