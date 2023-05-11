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
        sh 'npm install pm2 -g'
      }
    }  
    
    stage('Deploy') {
      steps {
         sh 'nohup node index.js > /dev/null 2>&1 &'
//         sh 'echo hello'
//         sh 'node index.js &'
//         sh 'sleep 10s'
      }
    } 
   
  }
}
