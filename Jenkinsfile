pipeline {
    agent { label 'AGENT-1'}
    environment {
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND'
        DEPLOY_TO = 'PRODUCTION'
    }
    options {
        disableConcurrentBuilds()

    }
    stages {
        stage('Build') {
            steps {
                script {
                sh '''
                    echo "Hello, this is build"
                    echo "project: $PROJECT"
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