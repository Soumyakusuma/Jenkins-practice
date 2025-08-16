pipeline{
    agent {
    label 'agent1'
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
}