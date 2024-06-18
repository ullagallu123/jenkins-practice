pipeline{
    agent{
        label 'node-20'
    }
    stages{
        stage("Checkout"){
            steps{
              echo "Fetch the code from github......"
            }
        }
        stage("Build"){
            steps{
                echo "Build the code....."
            }
        }
    }
}