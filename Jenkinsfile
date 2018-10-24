pipeline {
  agent any
  stages {
    stage('Begin Build') {
      steps {
        script {
          try {
            sh 'echo run mvn test'
            sh 'mvn test'
          } catch(Exception e) {
            currentBuild.result='FAILURE'
            throw e
          }
        }
      }
    }
  }
}