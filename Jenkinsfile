pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "Jenkins"
    } 
    stages {
        stage('Build') { 
            steps {
                script
                    sh """
                        echo "Building" 
                         echo $COURSE
                    """   
            }
        }
        stage('Test') { 
            steps {
                echo "Testing" 
            }
        }
        stage('Deploy') { 
            steps {
                echo "Deploying"
            }
        }
    }
    post{
        always{
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success {
            echo 'I will run if sucess'
        }
        failure {
            echo 'I will run if sucess'
        }
    }
}