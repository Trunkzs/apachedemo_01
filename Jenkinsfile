pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh 'docker exec jmeter-master -c "/opt/apache-jmeter-5.6.2/bin/jmeter -n -t SummaryReport.jmx -l TestResult.jtl -e -o /reports/"'
      }
    }

  }
}