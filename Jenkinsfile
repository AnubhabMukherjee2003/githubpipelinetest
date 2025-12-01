pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Installing npm dependencies..."
                sh '''
                npm i
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                npm test
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                npm run
                '''
            }
        }
    }
}