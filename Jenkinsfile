pipeline {
  agent any
  stages {
    stage('error') {
      agent any
      steps {
        sh '/opt/apache-jmeter-5.6.2/bin/jmeter -n -t SummaryReport.jmx -l /opt/result/TestResult-$BUILD_NUMBER.csv -e -o /opt/reports/$BUILD_NUMBER'
      }
    }

  }
}