pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Check python3 version
                sh 'python3 --version'
            }
        }
        stage("HTML Report") {
            steps {
                publishHTML (target: [
                    reportName: 'QA Table',
                    reportDir: '../../out',
                    reportFiles: 'index.html',
                    reportTitles: 'Rendering Library Comparison Table',
                    keepAll: true,
                    alwaysLinkToLastBuild: false,
                    allowMissing: true
                ])
            }
        }
    }
}
