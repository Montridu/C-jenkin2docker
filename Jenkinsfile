pipeline {
    
    agent any  

    environment {
        REGISTRY_URL = 'https://registry.mydomain.com'
        NODE_IMAGE = 'node:12.13.0'
        NODE_IMAGE_ARGS = '-u 0:0'
    }

    stages {
 
        stage('Init'){
            steps {
                echo 'Init'
                echo "build number : ${env.BUILD_NUMBER}"
                echo "registry url : ${env.REGISTRY_URL}"
            }
        }
 
        stage('Yarn Install') {
             agent {
                docker {
                    image "${env.NODE_IMAGE}"
                    args "${env.NODE_IMAGE_ARGS}"
                }
            }
            steps {
                echo 'Yarn Install'
                echo '******************************'  
                sh 'node --version'
                sh 'yarn --version'
            }
        }
         stage('Security') {
            steps{
                echo 'Security'
                echo 'Security1'
                echo '******************************'
            }
        }
        stage('Yarn Build') {
            steps {
                echo 'Yarn Build'
                echo '******************************'
            }
        }
 

        stage('Deploy') {
            steps{
                echo 'Deploy'
                echo '******************************'
            }
        }
    }
}
