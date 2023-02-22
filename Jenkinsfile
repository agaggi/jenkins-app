
pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }

    environment {
        DOCKER_TAG = sh 'git rev-parse --short HEAD'
        
    }

    stages {
        stage('Checkout') {
            steps {
                echo "${DOCKER_TAG}"
            }
        }
    }
}
