pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building..."
                echo "Task: Build the application, compile and package."
                echo "Tool: Maven"
            }
            post {
                always {
                    mail to: "leec8156@gmail.com",
                         subject: "Build Status Email",
                         body: "Build was successful"
                }
            }
        }
        stage("Test") {
            steps{
                echo "Testing..."
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying...."
            }
        }

        stage("Unit and Intergration Testing") {
            steps{
                echo "Testing..."
                echo "Task: Run unit tests and intergration tests."
                echo "Tool: Junit"
            }
        }
        stage("Code Analysis") {
            steps {
                echo "Analysing...."
                echo "Checking source code quality, maintainability, and coding standards"
                echo "Tool: SonarQube"
            }
        }
        stage("Security Scan") {
            steps{
                echo "Scanning...."
                echo "Checking for vulnerabilties."
                echo "Tool: OWASP ZAP"
            }
        }        
        stage("Deploy to Staging") {
            steps {
                echo "Staging...."
                echo "Deploying to pre-production environment."
                echo "Tool: AWS EC2"
            }
        }        
        stage("Intergration Tests on Staging") {
            steps {
                echo "Intergration tests...."
                echo "Testing within staging environment to predict production behaviour."
                echo "Tool: Selenium"
            }
        }
        stage("Deploy to Production") {
            steps {
                echo "Deploying..."
                echo "Deploying to Production environment."
                echo "Tool: AWS EC2"
            }
        }
    }
}
