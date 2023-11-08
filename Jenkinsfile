pipeline {
  agent any
  stages {
    stage('') {
      steps {
        sh 'jmeter -n -t SummaryReport.jmx -l TestResult.jtl -e -o /reports/'
      }
    }

  }
}