pipeline {
    agent any

    stages {
        stage('Build and Test') {
            parallel {
                stage('Build') {
                    stages {
                        stage('Compile') {
                            steps {
                                echo 'Compiling...'
                                sh 'echo "Compiling source code..."'
                                sleep 2
                            }
                        }
                        stage('Package') {
                            steps {
                                echo 'Packaging...'
                                sh 'echo "Creating package..." && mkdir -p build && touch build/app.jar'
                                sleep 2
                            }
                        }
                    }
                }
                stage('Test') {
                    stages {
                        stage('Unit Tests') {
                            steps {
                                echo 'Running Unit Tests...'
                                sh 'echo "Running unit tests..." && sleep 1'
                                sleep 2
                            }
                        }
                        stage('Integration Tests') {
                            steps {
                                echo 'Running Integration Tests...'
                                sh 'echo "Running integration tests..." && sleep 1'
                                sleep 2
                            }
                        }
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo "Deploying to test environment..." && mkdir -p deploy && touch deploy/dep
