pipeline {
    agent any

    environment {
        CI = 'true'
    }

    stages {

        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                echo 'Running unit tests...'
                bat 'npm test -- --watchAll=false'
            }
        }
    }
}
