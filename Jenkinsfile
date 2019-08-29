pipeline {
  agent any
  stages {
    stage('Install dependencies') {
      steps {
        sh 'apk add nodejs'
        sh 'echo $PATH'
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh '''cd TestAppiumDir
npm test'''
      }
    }
  }
  tools {
    nodejs 'node'
  }
}