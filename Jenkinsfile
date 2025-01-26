pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-repo/CalculatorApp.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t calculator-app src/.'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8080:80 --name calculator-app calculator-app'
            }
        }
        stage('Test Application') {
            steps {
                sh 'curl -I http://localhost:8080'
            }
        }
        stage('Cleanup') {
            steps {
                sh 'docker stop calculator-app && docker rm calculator-app'
            }
        }
    }
}
