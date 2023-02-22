def PIPELINE_ERROR = false


pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }

    environment {
        # Use the head of the commit hash for 'unique' tags 
        DOCKER_TAG = sh(script: 'git rev-parse --short HEAD', returnStdout: true)
        
        NEW_VERSION = '1.3.0'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out UI/UX'
                sh 'python3 main.py'


            }
        }

        stage ('Compile') {
            # when { expression { !PIPELINE_ERROR } }

            steps {
                echo 'Yo'
            }
        }
    }
}
