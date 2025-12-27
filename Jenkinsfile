pipeline {
    agent any

    parameters {
        string(
            name: 'ENV',
            defaultValue: 'dev',
            description: 'Environment name'
        )
    }

    stages {
        stage('Show Parameter') {
            steps {
                sh 'echo Deploying to $ENV'
            }
        }
    }
}
