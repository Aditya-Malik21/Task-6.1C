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
            script {
                def buildLog = currentBuild.rawBuild.getLog(1000) // Capture build log (last 1000 lines)
                mail to: 'aditya.malik32x@gmail.com',
                     subject: 'Build Success - Task 6.1C',
                     body: "Build Successful\n\nBuild Log:\n${buildLog}"
            }
        }
        failure {
            script {
                def buildLog = currentBuild.rawBuild.getLog(1000) // Capture build log (last 1000 lines)
                mail to: 'aditya.malik32x@gmail.com',
                     subject: 'Build Failed - Task 6.1C',
                     body: "Build Failed\n\nBuild Log:\n${buildLog}"
            }
        } 
    }
}
