pipeline {
  agent any
  tools {
        nodejs "nodejs"
    }
  stages {
      
    stage('Build') {
      steps {
        sh 'echo hello-world'
        sh 'sleep 5s'
        sh 'npm install'
        sh 'npm fund'
      }
    }  
    
    stage('Deploy') {
      steps {
        node index.js    
      }
    } 
   
  }
}
