pipeline {
    agent {
        label 'NodoEsclavo'
    }
    stages {
       stage('Checkout-git'){
              steps {
               git poll: true, url: 'https://github.com/AzuladoToujours/jenkins-CS.git'    
              }
       }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                 sh 'npm test'
            }
        }
        stage('Run App'){
            steps{
                sh 'npm start'
            }
        }
    }
}

