pipeline {
  agent {
    label "docker-slave"
  }
  tools {
        nodejs "19.8.1"
    }
  stages {
      
    stage('Build') {
      steps {
        sh 'echo hello-world'
        sh 'sleep 50m'
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
