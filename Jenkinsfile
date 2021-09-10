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
            }
        }
    }
    post {
        success {
            echo "success"
        }
    }
}
