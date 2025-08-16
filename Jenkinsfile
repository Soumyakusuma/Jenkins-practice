pipeline{
    agent {
    label 'agent1'
    }
}

    stages{
        stage('Build'){
            steps{
                echo "building"
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