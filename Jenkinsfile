pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/Yartret/DocLean.git'
            }
        }
        stage('Build Docker image') {
            steps {
                script {
                    dockerImage = docker.build('Nginx', '.')
                }
            }
        }
        stage('Push Docker image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'docker login Username:warglok@gmail.com Password:Eligeri3') {
                        dockerImage.push('latest')
                    }
                }
            }
        }
    }
}
