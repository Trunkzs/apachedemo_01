pipeline {
  agent any
  stages {
    stage('error') {
      agent any
      steps {
        sh 'docker network ls '
      }
    }

    stage('pwd') {
      steps {
        sh 'pwd'
      }
    }

  }
}