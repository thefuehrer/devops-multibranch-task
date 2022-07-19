pipeline {
    agent any
      
    tools {nodejs "node"}
      
    stages {
  
      
      stage('Checkout code'){
       steps{
          checkout([$class: 'GitSCM', branches: [[name: '']], extensions: [], userRemoteConfigs: [[credentialsId: '38446af3-1536-45d0-9f2c-f79b92d095c3', url: 'https://github.com/thefuehrer/devops-multibranch-task.git']]])
         }
      }
               
      stage('Build') {
        steps {
          bat 'npm install'
        }
      }  
    }
  }