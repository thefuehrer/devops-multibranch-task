pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
             
    stage('Build') {
      steps {
        bat 'npm install'
      }
    }

    stage('Lint') {
      steps {
        bat 'npm run lint'
      }
    }  
                
    stage('Test') {
      steps {
        bat 'npm test'
      }
    }
  }
  post {
    always {
      emailext body: 'Build successfully', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Jenkins'
      }
    }
  }
