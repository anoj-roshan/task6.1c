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
                    emailext (
                        attachmentsPattern: 'test-output.log',
                        body: 'The Unit Testing and Integration testing completed successfully',
                        subject: 'Unit and Integration Testing Status: SUCCESS',
                        to: 'sulaianoj232001@gmail.com'
                    )
                }
                failure {
                    emailext (
                        attachmentsPattern: 'test-output.log',
                        body: 'The Unit Testing and Integration testing completed unsuccessfully. Please check logs!',
                        subject: 'Unit and Integration Testing Status: FAILURE',
                        to: 'sulaianoj232001@gmail.com'
                    )
                }

        }
        always {
            echo 'Pipeline completed.'
        }
    }
