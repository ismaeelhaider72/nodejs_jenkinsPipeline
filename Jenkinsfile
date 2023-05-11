pipeline {
  agent any
  tools {
        nodejs "nodejs"
    }
  stages {
      
    stage('Build') {
      steps {
        sh 'echo hello-world'
        sh 'npm config set false --global'
        sh 'npm config set fund false'
        sh 'npm install'
      }
    }  
    
    stage('Deploy') {
      steps {
         sh 'echo hello'
         sh 'nohup node index.js >/dev/null 2>&1 &'
        // sh 'node index.js'
//         sh 'echo hello'
//         sh 'node index.js &'
//         sh 'sleep 10s'
      }
    } 
   
  }
}
