pipeline {
  agent {
    docker {
      image 'node:18-alpine'
      args '-u root:root'
    }
  }

  stages {
    stage('Install') {
      steps { sh 'npm install' }
    }
    stage('Test') {
      steps { sh 'npm test -- --watch=false' }
    }
    stage('Build') {
      steps { sh 'npm run build' }
    }
  }
}