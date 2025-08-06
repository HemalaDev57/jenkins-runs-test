pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sleep 20
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sleep 10
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sleep 5
                 // Fail the build
                error('Tests failed!')
            }
        }
    }
}
