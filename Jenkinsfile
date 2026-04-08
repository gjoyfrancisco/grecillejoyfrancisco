pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running unit tests...'
                bat 'set CI=true && npm test -- --watchAll=false'
            }
        }
    }
}
