pipeline {
    agent any
    
    environment {
        STAGE_NAME = ""
        BUILD_STATUS = "SUCCESS"
    }

    stages {
        
        stage('Build') {
            steps {
                script {
                    STAGE_NAME = "Build"
                }
                echo "Building the project using Maven"
                // Example Maven build command
                sh 'mvn clean install'
            }
            post {
                failure {
                    script {
                        BUILD_STATUS = "FAILURE"
                    }
                    echo "Build stage failed"
                }
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                script {
                    STAGE_NAME = "Unit and Integration Tests"
                }
                echo "Running unit and integration tests using JUnit and Selenium"
                // Example command to run tests
                sh 'mvn test'
            }
            post {
                success {
                    emailext(
                        to: 'your-email@example.com',
                        subject: "Stage ${STAGE_NAME} - ${BUILD_STATUS}",
                        body: "The ${STAGE_NAME} stage has ${BUILD_STATUS}.",
                        attachLog: true
                    )
                }
                failure {
                    script {
                        BUILD_STATUS = "FAILURE"
                    }
                    emailext(
                        to: 'your-email@example.com',
                        subject: "Stage ${STAGE_NAME} - ${BUILD_STATUS}",
                        body: "The ${STAGE_NAME} stage has failed. Please check the attached logs.",
                        attachLog: true
                    )
                }
            }
        }

        stage('Code Analysis') {
            steps {
                script {
                    STAGE_NAME = "Code Analysis"
                }
                echo "Performing code analysis using SonarQube"
                // Example SonarQube analysis command
                sh 'mvn sonar:sonar'
            }
            post {
                failure {
                    script {
                        BUILD_STATUS = "FAILURE"
                    }
                    echo "Code Analysis stage failed"
                }
            }
        }

        stage('Security Scan') {
            steps {
                script {
                    STAGE_NAME = "Security Scan"
                }
                echo "Conducting a security scan using OWASP ZAP"
                // Example OWASP ZAP command
                sh 'zap-cli quick-scan --self-contained --start-options "-config api.disablekey=true" http://your-app-url'
            }
            post {
                success {
                    emailext(
                        to: 'your-email@example.com',
                        subject: "Stage ${STAGE_NAME} - ${BUILD_STATUS}",
                        body: "The ${STAGE_NAME} stage has ${BUILD_STATUS}.",
                        attachLog: true
                    )
                }
                failure {
                    script {
                        BUILD_STATUS = "FAILURE"
                    }
                    emailext(
                        to: 'your-email@example.com',
                        subject: "Stage ${STAGE_NAME} - ${BUILD_STATUS}",
                        body: "The ${STAGE_NAME} stage has failed. Please check the attached logs.",
                        attachLog: true
                    )
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                script {
                    STAGE_NAME = "Deploy to Staging"
                }
                echo "Deploying the application to the staging environment"
                // Example deployment command
                sh 'scp target/your-app.jar user@staging-server:/path/to/deploy'
            }
            post {
                failure {
                    script {
                        BUILD_STATUS = "FAILURE"
                    }
                    echo "Deploy to Staging stage failed"
                }
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                script {
                    STAGE_NAME = "Integration Tests on Staging"
                }
                echo "Running integration tests on the staging environment"
                // Example integration tests command
                sh 'mvn verify -Pstaging'
            }
            post {
                failure {
                    script {
                        BUILD_STATUS = "FAILURE"
                    }
                    echo "Integration Tests on Staging stage failed"
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                script {
                    STAGE_NAME = "Deploy to Production"
                }
                echo "Deploying the application to the production environment"
                // Example production deployment command
                sh 'scp target/your-app.jar user@production-server:/path/to/deploy'
            }
            post {
                failure {
                    script {
                        BUILD_STATUS = "FAILURE"
                    }
                    echo "Deploy to Production stage failed"
                }
            }
        }
    }

    post {
        always {
            echo "Pipeline completed. Build status: ${BUILD_STATUS}"
        }
    }
}
