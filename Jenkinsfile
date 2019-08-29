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
        sh '''/usr/local/bin/appium &
cd TestAppiumDir
npm test'''
      }
    }
  }
  tools {
    nodejs 'node'
  }
}