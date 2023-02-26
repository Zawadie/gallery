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
    stage ('Run tests'){
            steps{
                sh 'npm test'
            }
        }
        stage ('Deploy to Render'){
            steps{
                httpRequest (httpMode:'POST',responseHandle:'NONE',url:'https://api.render.com/deploy/srv-cftncmp4reb6ks0vs8u0?key=gzo0lOolY48',wrapAsMultiPart:false)
            }
        }
        
    
    
}
}


  