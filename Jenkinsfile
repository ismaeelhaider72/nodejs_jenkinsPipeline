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
        sh 'npm install'
        sh 'npm install -g pm2'
        sh 'pm2 start index.js'
//         sh 'nohup node index.js > /dev/null 2>&1 &'
//         sh 'ps -ef | grep node'
//         sh 'node index.js'
//         sh 'nohup node index.js &'
        sh 'ps -ef | grep node'
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
