pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/vhoang88/myflaskapp.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myflaskapp:latest .'
            }
        }

pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/vhoang88/myflaskapp.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myflaskapp:latest .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker stop myflaskapp || true'
                sh 'docker rm myflaskapp || true'
                sh 'docker run -d -p 5000:5000 --name myflaskapp myflaskapp:latest'
            }
        }
    }

    post {
        always {
            sh 'docker ps -a'
        }
    }
}
        stage('Run Docker Container') {
            steps {
                sh 'docker stop myflaskapp || true'
                sh 'docker rm myflaskapp || true'
                sh 'docker run -d -p 5000:5000 --name myflaskapp myflaskapp:latest'
            }
        }
    }

    post {
        always {
            sh 'docker ps -a'
        }
    }
}
