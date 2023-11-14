pipeline {
  agent any
  stages {
    stage('Run Jmeter test') {
      steps {
        sh 'docker exec jmeter-master bash -c "/opt/apache-jmeter-5.6.2/bin/jmeter -n -t /opt/github/apachedemo_01/SummaryReport.jmx -l /opt/result/TestResult-$BUILD_NUMBER.csv -e -o /opt/reports/$BUILD_NUMBER"'
        sh 'docker cp jmeter-master:/opt/reports/$BUILD_NUMBER /opt/reports/$BUILD_NUMBER'   
    }
    }
 }
 post {
        always {  
            publishHTML target: [
                reportName: 'Test',
                reportDir: '/opt/reports/$BUILD_NUMBER',
                reportFiles: 'index.html', 
                reportTitles: 'Jmeter-report', 
                keepAll: true,
                alwaysLinkToLastBuild: true,
                allowMissing: false
            ]  
        }
}

}
