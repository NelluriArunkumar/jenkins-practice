pipeline {
    agent {
        label 'AGENT-1'
    }
    
    //Build
    stages {
        stage('Build'){
            steps{
                script{
                    echo 'Bulding..'
                }
            }
        }
        stage('Test'){
            steps{
                script{
                    echo 'Testing..'
                }
            }
        }
        stage('Deploy'){
            steps{
                script{
                    echo 'Deploying..'
                }
            }
        }
    }

    post {
        always {
            echo 'I will always say hello again'
            deleteDir()
        }

        success {
            echo 'Hello Success'
        }

        failure {
            echo "Hello Failure"
        }
    }
}