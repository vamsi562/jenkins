pipeline{
    // agent any - it will run job in master
    agent{
        node{
            label 'agent-1'
        }
    } // asking jenkins to run pipeline in agent-1 node
    environment{
        // environment variable declaration, which can be accessed across all stages
        Course = 'DevOps'
        Module = 'Jenkins'
    }
    stages{
        stage('Build'){
            steps{
                script{
                    sh """
                        echo 'Building Job'
                        echo 'Course name is ${Course}'
                    """
                }
                
            }
        }
        stage('Test'){
            steps{
                script{
                    sh """
                        echo 'testing job'
                    """
                }
            }
        }
        stage('Deploy'){
            steps{
                script{
                    sh """
                        echo 'Deploying Job'
                    """
                }
            }
        }
    }
    post{ // post deployment action - execute after above stages 
        always{ // this block will always execute after all stages whether success or failure
            cleanWs()
        }
        success{ // if all stages are successful then execute this block
            echo 'succeeded'
        }
        failure{ // if any stage fails then execute this block
            echo 'failed'
        }
    }
}