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
         bat 'move /dist/line-cruise/* /var/www/html'
      }
    }       
  }
}