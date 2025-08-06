pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sleep 20
            }
        }
        stage('Build') {
            steps {
                echo 'Building..' 
                sleep 10
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sleep 5
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sleep 15
            }
        }
    }
}
