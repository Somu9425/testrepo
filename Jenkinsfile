pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Somu9425/testrepo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-world .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run --rm hello-world'
            }
        }
    }
}
