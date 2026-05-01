pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build: Build the code using Maven to compile and package the code.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Unit and Integration Tests: Run unit and integration tests using JUnit and Selenium.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code Analysis: Analyse the code using SonarQube to check code quality and standards.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Security Scan: Scan the code using OWASP Dependency-Check to identify vulnerabilities.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to Staging: Deploy the application to an AWS EC2 staging server.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration Tests on Staging: Run integration tests on staging using Postman/Newman.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production: Deploy the application to an AWS EC2 production server.'
            }
        }
    }
}