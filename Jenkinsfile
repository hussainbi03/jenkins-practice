pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                    echo "Hello, this is build"
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                    echo "Hello, this is test"
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                    echo "Hello, this is deploy"
                '''
            }
        }
    }
}