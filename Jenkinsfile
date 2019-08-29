pipeline {
  agent any
  stages {
    stage('Install dependencies') {
      steps {
        sh '''apk add nodejs
echo $PATH
cd TestAppiuDir
npm install'''
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
  }
  tools {
    nodejs 'node'
  }
}