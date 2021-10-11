pipeline{
  agent { label 'demonode'}
   environment {
        IMAGE_TAG = "${env.BUILD_NUMBER}"
        
  }

stages{

   stage('SCM Checkout'){
     steps{
 git 'https://github.com/saronavee/simple-web-app.git'
     }
   }
                        
   stage('Unit Testing'){
     steps{
             sh label: '', script: 'mvn clean test'
     }
   }
      stage('Maven packing'){
     steps{
           sh label: '', script: 'mvn clean package'
        }
    }
    
   stage('Input') {
            steps {
                input('Do you want to proceed to dev?')
            }            
            
    }

    stage('Onput') {
            steps {
                input('Do you want to proceed to dev?')
            }            
            
    }

    
}
}
           
