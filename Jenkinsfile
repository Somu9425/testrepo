pipeline {
    agent any

    environment {
        IMAGE_NAME = "hello-world"
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Somu9425/testrepo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t $IMAGE_NAME .'
                }
            }
        }
    }

    post {
        success {
            echo "✅ Docker image built successfully!"
        }
        failure {
            echo "❌ Build failed!"
        }
    }
}

