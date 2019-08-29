pipeline {
  agent any
  stages {
    stage('Install dependencies') {
      steps {
        sh '''apk add nodejs
echo $PATH
npm install'''
      }
    }
    stage('Test') {
      steps {
        sh '''#!/bin/bash
npm test'''
      }
    }
  }
  tools {
    nodejs 'node'
  }
}