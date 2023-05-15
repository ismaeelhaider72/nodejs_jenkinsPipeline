pipeline {
  agent any
  tools {
        nodejs "nodejs"
    }
  stages {
    stage('Job 1') {
            steps {
                // Run Job 1 and capture the parameters
                script {
                    def job1Parameters = [
                        string(name: 'name', value: 'ismaeel'),
                        booleanParam(name: 'cast', value: 'qureshi')
                        // Add other parameters as needed
                    ]
                    build job: 'Job_1', parameters: job1Parameters
                }
            }
        }
        stage('Job 2') {
            steps {
                // Run Job 2 and pass parameters from Job 1 as environment variables
                script {
                    def job2Parameters = [
                        string(name: 'name', value: "${env.name}"),
                        booleanParam(name: 'cast', value: "${env.cast}")
                        // Add other parameters as needed
                    ]
                    build job: 'Job_2', parameters: job2Parameters
                }
            }
        }
      
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
