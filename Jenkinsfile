pipeline {
  agent any
  stages {
    stage('Install dependencies') {
      steps {
        sh '''apk add nodejs
echo $PATH
cd TestAppiumDir
npm install
#!/bin/bash --login -x
appium &
'''
      }
    }
    stage('Test') {
      steps {
        sh '''cd TestAppiumDir
sleep 5s
npm test'''
      }
    }
  }
  tools {
    nodejs 'node'
  }
}