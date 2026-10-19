pipeline{
    // agent any - it will run job in master
    agent{
        label 'agent-1'
    } // asking jenkins to run pipeline in agent-1 node
    stages{
        stage('Build'){
            steps{
                echo 'Building Job'
            }
        }
        stage('Test'){
            steps{
                echo 'testing job'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploying Job'
            }
        }
    }
    post{
        always{
            cleanWS()
        }
        success{
            echo 'succeeded'
        }
        failure{
            echo 'failed'
        }
    }
}