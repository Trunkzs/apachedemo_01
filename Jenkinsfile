pipeline {
  agent any
  stages {
    stage('Run Jmeter test') {
      steps {
        sh '/opt/apache-jmeter-5.6.2/bin/jmeter -n -t SummaryReport.jmx -l /opt/result/TestResult-$BUILD_NUMBER.csv -e -o /opt/reports/$BUILD_NUMBER'
      }
    }

    stage('HTML Report') {
      steps {
        script {
          publishHTML([allowMissing: false, alwaysLinkToLastBuild: true, reportDir: 'opt/reports/$BUILD_NUMBER', reportFiles: 'index.html'])
        }

      }
    }

  }
}