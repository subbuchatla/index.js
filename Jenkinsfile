pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run tests here if you have any
                    echo 'Running tests...'
                }
            }
        }
        stage('Build') {
            steps {
                // Run the build script using npm
                bat 'npm run build'
            }
        }
        stage('Build Docker Image') {
            steps {
                // Build Docker image for the application
                bat 'docker build -t my-node-app:1.0 .'
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Echo deployment message (customize for actual deployment steps)
                    echo 'Deploying application...'
                }
            }
        }
    }
}
