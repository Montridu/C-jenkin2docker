pipeline {
    
    agent {
        any { 
            image 'node:12.16.2' 
            args '-p 3000:3000' 
        }
    }  

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
        stage('Build') {
            steps {
                sh 'node --version'
                sh 'npm install'
                sh 'npm run build'
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