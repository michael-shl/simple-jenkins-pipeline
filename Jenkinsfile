pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git url: 'https://github.com/michael-shl/simple-jenkins-pipeline.git', branch: 'master'
                // Run shell script
                sh "python3 --version"
            }
        }
        stage("Report") {
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
