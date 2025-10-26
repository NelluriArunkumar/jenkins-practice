pipeline {
    agent {
        label 'AGENT-1'
    }

    environment {
        COURSE = 'Jenkins'
    }

    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds() //It is used to disable the parallel Builds of the job
    }
    
    //Build
    stages {
        stage('Build'){
            steps{
                script{
                    sh """
                        echo 'Helo Bulid'
                        env
                    """
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