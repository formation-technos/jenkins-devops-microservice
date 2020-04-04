pipeline {
 agent any
 //agent {
   //     docker { image 'maven:3.6.3' }
    //}
	environment {
	     dockerHome = tool 'MyDocker'
		 mavenHome = tool 'myMaven'
		 PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
  stages { 
  
       stage('Checkout'){
	      steps{
		     sh 'mvn --version'
			 sh 'docker --version'
		    echo "Build"
			echo"Path : $PATH"
			echo"Build_NUMBER : $env.BUILD_NUMBER"
			echo"Build_NUMBER : $env.BUILD_NUMBER"
			echo"Build_ID : $env.BUILD_ID"
			echo"Build_TAG : $env.BUILD_TAG"
			echo"Build_URL : $env.BUILD_URL"
			echo"JOB_NAME : $env.JOB_NAME"
			
		  }
	   }
	   stage('Compile'){
	         steps{
		      sh "mvn clean compile"
		     }   
	   }
	   
		  stage('Test'){
	         steps{
		        sh "mvn test"
		     }   
	   }
	   
	   stage('Integration Test'){
	      steps{
		    echo "Integration Test"
		  }	   
	   }		  		  
	}
  post {
		 always {
		     echo " i run always"
		 
		 }
		success {
		      echo " it all ok succes "
		
		}
		failure {
		      echo " it failure !!! "
		
		}		
	}
}