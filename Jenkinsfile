pipeline {
  agent any
  
  tools {nodejs "node"}
  
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
        sh 'cd TestAppiumDir'
        sh 'npm test'
      }
    }
  }
}
