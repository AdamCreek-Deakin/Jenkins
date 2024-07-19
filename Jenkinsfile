pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Stage 1:'
                echo 'Build Automation Tool: '
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests: '
                echo 'Test Automation Tool:'
            }
            post {
                success {
                    //emailext attachLog: true, 
					to: 'a.creek@bigpond.com',
					subject: 'Unit and Integration Test: Success', 
					body: 'Stage 2 successfully implemented. Refer Report.' 
                }
                failure {
                    //emailext attachLog: true, 
					to: 'a.creek@bigpond.com',
					subject: 'Unit and Integration Test: Failure', 
					body: 'Stage 2 unsuccessfully implemented. Refer Report.' 
                }
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis: '
                echo 'Code Analysis Tool:
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan : '
                echo 'Security Scan Tool:'
            }
            post {
                success {
                    //emailext attachLog: true, 
					to: 'a.creek@bigpond.com',
					subject: 'Security Scan Test: Success', 
					body: 'Stage 4 successfully implemented. Refer Report.' 
                }
                failure {
                    //emailext attachLog: true, 
					to: 'a.creek@bigpond.com',
					subject: 'Security Scan Test: Failure', 
					body: 'Stage 4 unsuccessfully implemented. Refer Report.' 
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging: '
                echo 'Deployment Tool:'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging: '
                echo 'Integration Testing Tool:'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production: '
                echo 'Production Deployment Tool:'
            }
        }
    }
}
