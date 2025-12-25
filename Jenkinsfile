pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "Jenkins"
    } 
    options {
        timeout(time: 10, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') { 
            steps {
                script{
                    sh """
                        echo "Building" 
                        echo $COURSE
                        sleep 10
                        env
                    """  
                } 
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
        aborted {
             echo 'pipeline is aborted'
        }
        }
    }
}