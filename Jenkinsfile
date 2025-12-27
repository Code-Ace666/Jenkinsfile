pipeline {
    agent any

    parameters {
        choice(
            name: 'ENV',
            choices: ['dev', 'prod'],
            description: 'Select environment'
        )
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

        stage('Deploy to DEV') {
            when {
                expression { params.ENV == 'dev' }
            }
            steps {
                echo 'Auto deploy to DEV'
            }
        }

        stage('Approval for PROD') {
            when {
                expression { params.ENV == 'prod' }
            }
            steps {
                input message: 'Deploy to PROD?'
            }
        }

        stage('Deploy to PROD') {
            when {
                expression { params.ENV == 'prod' }
            }
            steps {
                echo 'Deploying to PROD'
            }
        }
    }
}
