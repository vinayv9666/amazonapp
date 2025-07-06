pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/vinayv9666/amazonapp.git'
            }
        }
        stage('Build Docker image') {
            steps {
                sh "docker build -t vinayv9666/amazonapp:v1 ."
            }
        }
        stage('Create Docker Container') {
            steps {
                sh "docker run -itd --name amazonapp -p 81:80 vinayv9666/amazonapp:v1"
            }
        }
    }
}
