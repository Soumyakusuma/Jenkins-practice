pipeline{
    agent {
    label 'agent1'
    }
     environment { 
        COURSE = 'jenkins'
    }
    options {
        timeout(time: 10, unit: 'SECONDS') 
        disableConcurrentBuilds()
    }

    stages{
        stage('Build'){
            steps{
                script{
                    sh """
                    echo "Hello Build this is $COURSE"
                    sleep 10
                    env
                    """
                }
            }
        }
        stage('Test'){
            steps{
                echo "testing"
            }
        }
        stage('deploy'){
            steps{
                echo "deploying"
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'Hello Success'
        }
        changed { 
            echo 'Hello Failure'
        }
    }

}