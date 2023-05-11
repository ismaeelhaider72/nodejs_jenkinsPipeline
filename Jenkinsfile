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
        script {
          def command = "nohup node index.js > output.log 2>&1 & echo $!"
          def pid = sh(script: command, returnStdout: true).trim()
          sh "echo Node.js command started with PID ${pid}"
        }
//         sh 'echo hello'
//         sh 'node index.js &'
//         sh 'sleep 10s'
      }
    } 
   
  }
}
