pipeline {
  agent any
  stages {
    stage('Install dependencies') {
      steps {
        sh '''#!/bin/bash
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