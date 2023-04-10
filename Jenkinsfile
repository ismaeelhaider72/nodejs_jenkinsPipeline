pipeline {
  agent any
  tools {
        nodejs "19.8.1"
    }
  stages {
        
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }  
    
    stage('Deploy') {
      steps {
        node index.js > app.out.log 2> app.err.log < /dev/null &     
      }
    } 
   
  }
}
