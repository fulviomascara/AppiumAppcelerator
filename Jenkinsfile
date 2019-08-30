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
        sh '''#!/bin/sh
appium &
sleep 10s
cd TestAppiumDir
npm test'''
      }
    }
  }
  tools {
    nodejs 'node'
  }
}