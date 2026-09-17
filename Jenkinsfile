pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/prabanjant2024a-hub/student-management-project2.git'
            }
        }
        stage('Generate Report') {
            steps {
                sh 'python3 app.py'
            }
        }
        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
