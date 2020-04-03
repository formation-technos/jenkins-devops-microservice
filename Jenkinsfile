
pipeline {
  agent any
  stages {
  
  
       stage('Build'){
	      steps{
		    echo "Build"
		  }
	   
	   }
          
		  
		  stage('Test'){
	      steps{
		    echo "Test"
		  }
	   
	   }
	   
	   stage('Integration Test'){
	      steps{
		    echo "Integration Test"
		  }
	   
	   }
		  
	    post {
		 always {
		     echo " i run always"
		 
		 }
		succes {
		      echo " it all ok succes "
		
		}
		failure {
		      echo " it failure !!! "
		
		}
		
		
		
		}
		  
		  
	}
  



}