pipeline {
    
   agent any

   stages {

       stage ('Git Checkout'){
             
          steps{ 
               git branch: 'test', url: 'https://github.com/Sandeep-git-go/demo-counter-app.git' 
          }

    }
       
       stage('UNIT Testing'){
          
          steps{

             sh 'mvn test'
          }

         }
       
       stage('Integration Testing'){

          steps{

             sh 'mvn verify -DskipUnitTests'
       }

    }
        
      stage('Maven Build'){

          steps{

             sh 'mvn clean install'
       }

    }


 }
}
