pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sleep 5
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sleep 5

                    // Mark this stage as UNSTABLE and stop further stages
                    catchError(buildResult: 'UNSTABLE', stageResult: 'UNSTABLE') {
                        error('Tests failed. Marking build as UNSTABLE and stopping pipeline.')
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sleep 5
            }
        }
    }
}
