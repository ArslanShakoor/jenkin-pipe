pipeline {
    agent any 
  tools {
    nodejs 'node js'
  }
  stages {
    stage('Startup') {
      steps {
        script {
          sh 'npm install'
        }
      }
    }
    stage('Test') {
      steps {
        script {
          sh 'npm test'
        }
      }
    }
    stage('Build') {
      steps {
        script {
          sh 'npm run build'
        }
      }
    }
  }
}
