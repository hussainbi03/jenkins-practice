pipeline {
    agent { label 'AGENT-1'}
    environment {
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND'
        DEPLOY_TO = 'PRODUCTION'
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 20, unit: 'MINUTES')

    }
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Build') {
            steps {
                script {
                sh '''
                    echo "Hello, this is build"
                    echo "project: $PROJECT"
                    echo "Hello ${params.PERSON}"

                    echo "Biography: ${params.BIOGRAPHY}"

                    echo "Toggle: ${params.TOGGLE}"

                    echo "Choice: ${params.CHOICE}"

                    echo "Password: ${params.PASSWORD}"
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