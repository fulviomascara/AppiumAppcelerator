pipeline {
  agent any
  stages {
    stage('Install dependencies') {
      steps {
        sh '''apk add nodejs
echo $PATH
cd TestAppiumDir
npm install'''
      }
    }
    stage('Test') {
      steps {
        sh '''cd TestAppiumDir
appium &
sleep 10s
npm test'''
      }
    }
  }
  tools {
    nodejs 'node'
  }
}