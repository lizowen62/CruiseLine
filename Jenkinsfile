pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Install dependencies') {
      steps {
        bat 'npm install'
      }
    }
     
    stage('build') {
      steps {
         bat 'npm run ng -- build --prod'
      }
    }

    stage('deploy') {
      steps {
         bat 'mv dist/cruise-line/* C:/wamp64/www/'
      }
    }       
  }
}