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
          sh 'npm audit fix'
        }
      }
    }
    stage('Test') {
      steps {
        script {
          sh 'npm test'
        }
      }
      post {
        always {
          junit 'output/coverage/junit/junit.xml'
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
