pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/Zawadie/gallery.git'
      }
    }
    stage('Build') {
      steps {
        sh 'npm install'
         
      }
    }
    
}
}