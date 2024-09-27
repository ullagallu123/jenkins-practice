pipeline{
    agent any
    stages{
        stage("Checkout"){
            steps{
                echo "Checkout the code successfully..."
            }
        }
        stage("Source Code Analysis & Owasp Despendency Check"){
            parallel{
                stage("Source Code Analysis"){
                    steps{
                      echo "Source Code Analysis..."
                    }
                }
                stage("Owasp Dependency Check"){
                    steps{
                      echo "Owasp dependency Check..."
                    }
                }
            }
        }
        stage("Docker Build"){
            step{
                echo "Docker images Backing..."
            }
        }
        stage("Image Scanning"){
            steps{
               echo "Image Scanning........"
            }
        }
        stage("Push Image to ECR"){
            steps{
              echo "Successfully push image in to Repo"
            }
        }
    }
    // post {
    //     success {
    //         slackSend (channel: '#your-channel', color: 'good', message: "Build Succeeded: ${env.JOB_NAME} [${env.BUILD_NUMBER}] (<${env.BUILD_URL}|Open>)")
    //     }
    //     failure {
    //         slackSend (channel: '#your-channel', color: 'danger', message: "Build Failed: ${env.JOB_NAME} [${env.BUILD_NUMBER}] (<${env.BUILD_URL}|Open>)")
    //     }
    //     unstable {
    //         slackSend (channel: '#your-channel', color: 'warning', message: "Build Unstable: ${env.JOB_NAME} [${env.BUILD_NUMBER}] (<${env.BUILD_URL}|Open>)")
    //     }
    //     always {
    //         slackSend (channel: '#your-channel', color: '#439FE0', message: "Build Finished: ${env.JOB_NAME} [${env.BUILD_NUMBER}] (<${env.BUILD_URL}|Open>)")
    //     }
    // }
}