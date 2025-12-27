pipeline {
    agent any

    environment {
        ENV_NAME = "dev"
    }

    stages {
        stage('Show Env') {
            steps {
                sh 'echo Environment is $ENV_NAME'
            }
        }
    }
}
