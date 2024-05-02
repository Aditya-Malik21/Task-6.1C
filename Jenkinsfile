pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                echo 'Task: Build the code'
                echo 'Tool Example: Maven (mvn package)' 
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Execute Unit & Integration Tests'
                echo 'Tool Examples: JUnit, TestNG, Mockito' 
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Perform Code Analysis'
                echo 'Tool Examples: SonarQube, Checkstyle, PMD'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Perform Security Analysis'
                echo 'Tool Examples: OWASP ZAP, Snyk' 
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy to Staging Environment'
                echo 'Tool Examples: Ansible, AWS CLI' 
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Integration Tests on Staging'
                echo 'Tool Examples: Selenium, Cypress' 
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy to Production Environment'
                echo 'Tool Examples: AWS CLI, Terraform' 
            }
        }
    }

    post {
        success {
            emailext body: 'Build Successful: Check console output at $BUILD_URL', 
                     subject: 'Build Success - Project Name', 
                     to: 's223852007@deakin.edu.au' 
        }
        failure {
            emailext body: 'Build Failed: Check console output at $BUILD_URL', 
                     subject: 'Build Failed - Project Name', 
                     to: 's223852007@deakin.edu.au' 
        } 
    }
}
