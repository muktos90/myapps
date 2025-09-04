
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/muktos90/myapps.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t myapps .'
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    sh 'docker run --rm myapps'
                }
            }
        }
    }
}
