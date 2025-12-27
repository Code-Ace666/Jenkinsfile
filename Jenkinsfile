pipeline {
    agent any

    stages {
        stage('Generate Artifact') {
            steps {
                sh '''
                mkdir -p output
                echo "Build number: $BUILD_NUMBER" > output/result.txt
                date >> output/result.txt
                '''
            }
        }
    }

    post {
        success {
            archiveArtifacts artifacts: 'output/*.txt'
        }
    }
}
