pipeline {
  agent any
  stages {
    stage('Run Jmeter test') {
      steps {
        sh 'docker exec -it jmeter-master bash -c "/opt/apache-jmeter-5.6.2/bin/jmeter -n -t SummaryReport.jmx -l /opt/result/TestResult-$BUILD_NUMBER.csv -e -o /opt/reports/$BUILD_NUMBER"'
      }
    }

  }
}