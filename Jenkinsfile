pipeline {
  agent any
//   tools {
//         nodejs "nodejs"
//     }
  stages {
      
    stage('Build') {
      steps {
        sh 'sudo apt-get update && sudo apt-get install -y nodejs npm'
        sh 'echo hello-world'
        sh 'npm config set false --global'
        sh 'npm config set fund false'
        sh 'npm install'
//         sh 'ps -ef | grep node'
        sh 'node index.js'
//         sh 'nohup node index.js &'
//         sh 'ps -ef | grep node'
      }
    }  
    
//     stage('Deploy') {
//       steps {
//          sh 'echo hello'
//          sh 'node index.js &'
//       }
//     } 
   
  }
}
