pipeline{
    agent{
        label 'node-20'
    }
    stages{
        stage("Checkout"){
            steps{
              echo "Download the code from github......"
              git branch: 'main', url: 'https://github.com/ullagallu123/jenkins-practice.git'
            }
        }
        stage("Build"){
            steps{
                echo "Build the code....."
            }
        }
        stage("Deploying"){
            steps{
                echo "Deploy the code"
            }
        }
    }
    post{
        always{
            echo "cleaning up..."
            deleteDir() //delete current build dir once build was completed
        }
    }
}