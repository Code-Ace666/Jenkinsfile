pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh '''
                docker build -t jenkins-docker-demo .
                '''
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker rm -f demo || true
                docker run -d -p 8085:80 --name demo jenkins-docker-demo
                '''
            }
        }
    }
}
