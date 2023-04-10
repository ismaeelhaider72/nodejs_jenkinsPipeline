pipeline {
  agent any
  tools {
        nodejs "19.8.1"
    }
  stages {
      
    stage('Build') {
      git branch: 'main', url: 'https://github.com/ismaeelhaider72/nodejs_jenkinsPipeline'
      steps {
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
