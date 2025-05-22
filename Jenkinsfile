pipeline {
    agent { label 'AGENT-1'}
    environment {
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND'
        DEPLOY_TO = 'QA'
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 20, unit: 'MINUTES')

    }
    // parameters{
    //     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    //     text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    //     booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    //     choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    //     password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    // }
    stages {
        stage('Build') {
            steps {
                script{
                    sh  '''
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
            // input {
            //     message "Should we continue?"
            //     ok "Yes, we should."
            //     submitter "alice,bob"
            //     // parameters {
            //     //     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            //     // }
            // } 
            when { 
                environment name: 'DEPLOY_TO', value: 'PRODUCTION'
            }
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