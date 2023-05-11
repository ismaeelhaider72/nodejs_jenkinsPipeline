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
      }
    }  
    
    stage('Deploy') {
      steps {
        node index.js    
      }
    } 
   
  }
}
