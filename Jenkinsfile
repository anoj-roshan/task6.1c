pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
                // Tool: Maven
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests...'
                echo 'Running integration tests...'
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Running code analysis...'
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging server...'
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production server...'
            }
        }
    }
    
    post {
        success {
            mail to: "sylvester25r@gmail.com",
                subject: "Build Status Email",
                body: "Build was successfull!"
        }
        failure {
            mail to: "sylvester25r@gmail.com",
                subject: "Build Status Email",
                body: "Build was Failure!"
        }
    }
}