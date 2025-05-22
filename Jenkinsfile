pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                sh '''
                    echo "Hello, this is build"
                '''
            }
            }
        }
        stage('Test') {
            steps {
                script {
                sh '''
                    echo "Hello, this is test"
                '''
            }
            }
            }

        stage('Deploy') {
            steps {
                script {
                sh '''
                    echo "Hello, this is deploy"
                '''
            }
            }
        post {
            always {
                echo "I will alwats say hello again"
            }
            failure {
                echo "pipeline has failed"
            }
            success {
                echo "pipeline is succesfully ran"
            }
        }    
            }

    }
}