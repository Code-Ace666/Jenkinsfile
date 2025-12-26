pipeline {
    agent any

    stages {
        stage('Clone Info') {
            steps {
                echo 'Repo cloned successfully'
            }
        }

        stage('Workspace Check') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Simple Test') {
            steps {
                sh 'echo "Pipeline is working"'
            }
        }
    }
}
