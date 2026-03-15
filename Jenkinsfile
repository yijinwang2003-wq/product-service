pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Running security scan'
            }
        }

        stage('Container Build') {
            steps {
                echo 'Building Docker image'
            }
        }

        stage('Container Push') {
            steps {
                echo 'Pushing image to Docker Hub'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to Kubernetes'
            }
        }
    }
}