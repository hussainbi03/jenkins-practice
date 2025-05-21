pipeline{
    agent any {
        stages{
            stage('Build') {
                script {
                    sh """
                        echo "Helo, this is build"
                      """  
                }
            }
           stage('Test') {
                script {
                    sh """
                        echo "Hello, this is test"
                    """    
                }
           } 
            stage('Deploy') {
                    script {
                        sh """
                            echo "Hello, this is deploy"
                        """    
                    }
            }

        }
    }

    
}