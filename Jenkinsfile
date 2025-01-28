pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository
                git 'https://github.com/your-username/CalculatorApp.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                // Build Docker image
                sh 'docker build -t calculator-app ./src'
            }
        }
        stage('Run Docker Container') {
            steps {
                // Run the container
                sh 'docker run -d -p 8080:80 --name calculator-app calculator-app'
            }
        }
        stage('Test Application') {
            steps {
                // Simple test to check if the app is running
                sh 'curl -I http://localhost:8080'
            }
        }
        stage('Cleanup') {
            steps {
                // Stop and remove the Docker container
                sh 'docker stop calculator-app || true'
                sh 'docker rm calculator-app || true'
            }
        }
    }
}
