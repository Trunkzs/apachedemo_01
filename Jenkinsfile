pipeline {
  agent any
  stages {
    stage('error') {
      agent any
      steps {
        sh 'docker exec jmeter-master bash'
      }
    }

    stage('pwd') {
      steps {
        sh 'pwd'
      }
    }

  }
}