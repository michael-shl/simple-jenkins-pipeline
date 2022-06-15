pipeline {
    agent any
    stages {
        stage('build') {
            steps {
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
