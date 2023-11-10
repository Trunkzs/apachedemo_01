pipeline {
    agent any
    stages {
        stage('error') {
            agent any
            steps {
                script {
                    // Run JMeter test
                    sh "/opt/apache-jmeter-5.6.2/bin/jmeter -n -t SummaryReport.jmx -l /opt/result/TestResult-$BUILD_NUMBER.csv -e -o /opt/reports/$BUILD_NUMBER"
                    
                    // Publish HTML report
                    publishHTML(allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: "/opt/reports/$BUILD_NUMBER", reportFiles: 'index.html', reportName: 'jmeter', reportTitles: '')
                }
            }
        }
    }
}
