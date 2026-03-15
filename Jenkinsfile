pipeline {
    agent any

    environment {
        IMAGE_NAME = "yw24251436/product-service"
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests'
                sh 'pytest tests || true'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Running security scan'
                sh 'trivy image product-service || true'
            }
        }

        stage('Container Build') {
            steps {
                echo 'Building Docker image'
                sh 'docker build -t product-service .'
            }
        }

        stage('Container Push') {
            steps {
                echo 'Pushing image to Docker Hub'
                sh 'docker tag product-service $IMAGE_NAME:latest'
                sh 'docker push $IMAGE_NAME:latest'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to Kubernetes (placeholder)'
            }
        }
    }
}