pipeline {
  agent { 
        label "docker-slave"
     }
  tools {
        nodejs "nodejs"
    }
  stages { 
    stage('Build') {
      steps {
//         sh 'sudo apt-get update && sudo apt-get install -y nodejs npm'
        sh 'echo hello-world'
        sh "echo ${params.job2Parameters}"
        sh 'npm install'
         // installing
//         sh 'npm install -g forever'
//         sh 'node index.js'
//         sh 'nohup node index.js > /dev/null 2>&1 &'
           sh 'nohup node index.js > app.log 2>&1 &'
//         sh 'ps -ef | grep node'
//         sh 'node index.js'
//         sh 'nohup node index.js &'
        sh 'ps -ef | grep node'
      }
    }  
    stage('echoing'){
      steps {
       sh "echo ${params.city}"
      }
    }
    stage('Deploy') {
      steps {
         sh 'echo hello'
         sh 'sleep 5s'
         sh 'ps -ef | grep node'
      }
    } 
   
  }
}
