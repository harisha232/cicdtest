pipeline {
    agent any
    environment {
        RELEASE='20.04'
    }
    stages {
        stage('build') {
            environment {
            LOG_LEVEL='INFO'
             }
            steps {
                echo "current release $RELEASE and loglevel $LOG_LEVEL"
            }
        }
        stage('Test') { 
            steps { 
                echo "Testing release $RELEASE"
                writeFile file:'test-results.txt', text: 'passed'
            }
        }
    }
    post {
        success {
            archiveArtifacts "test-results.txt"
        }
    }
}
