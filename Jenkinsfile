pipeline {
    agent {
        docker {
            image 'docker:latest'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Dhymwhy/PROJECT'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t my-html-project .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run -d -p 8081:80 my-html-project'
                }
            }
        }
    }
}
