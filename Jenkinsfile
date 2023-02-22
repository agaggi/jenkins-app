
pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }

    environment {
        DOCKER_TAG = git rev-parse --short HEAD
        
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
