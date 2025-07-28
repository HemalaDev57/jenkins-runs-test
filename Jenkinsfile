pipeline {
    agent any

    triggers {
        cron('H * * * *') // Every 1hr
    }

    stages {
        stage('Hourly Task') {
            steps {
                echo "Running hourly job at: ${new Date()}"
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
