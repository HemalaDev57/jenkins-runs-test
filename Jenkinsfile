pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sleep 2
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Fail the build
                error('Tests failed!')
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sleep 2
            }
        }
    }
}
