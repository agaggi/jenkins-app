
pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }

    environment {
        DOCKER_TAG = sh(script: 'git rev-parse --short HEAD', returnStdout: true).trim()
        
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out'
                echo "This is ${DOCKER_TAG}"
            }
        }
    }
}
