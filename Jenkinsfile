pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
               
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests...'
                
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing Code...'
               
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing Security Scan...'
                
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging...'
                
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging...'
                
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                
            }
        }
    }
    post {
        success {
            mail to: 'anojroshan23@outlook.com',
                 subject: "SUCCESS: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                 body: "Build ${env.BUILD_NUMBER} of ${env.JOB_NAME} was successful."
        }
        failure {
            mail to: 'anojroshan23@outlook.com',
                 subject: "FAILURE: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                 body: "Build ${env.BUILD_NUMBER} of ${env.JOB_NAME} failed. Check Jenkins for details."
        }
        always {
            echo 'Pipeline completed.'
        }
    }
}