pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add build steps here
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests...'
                // Add test steps here
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing Code...'
                // Add code analysis steps here
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing Security Scan...'
                // Add security scan steps here
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging...'
                // Add deployment steps here
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging...'
                // Add integration test steps here
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                // Add production deployment steps here
            }
        }
    }
    post {
        success {
            emailext(
                replyto: 'sulaianoj232001@gmail.com',
                subject: "SUCCESS: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                body: "Build ${env.BUILD_NUMBER} of ${env.JOB_NAME} was successful.",
                attachLog: true
            )
        }
        failure {
            emailext(
                replyto: 'sulaianoj232001@gmail.com',
                subject: "FAILURE: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                body: "Build ${env.BUILD_NUMBER} of ${env.JOB_NAME} failed. Check Jenkins for details.",
                attachLog: true
            )
        }
        always {
            echo 'Pipeline completed.'
        }
    }
}
