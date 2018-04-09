pipeline {
      	agent any
	      options {
		             disableConcurrentBuilds()
           }
	
	 stages{
		    stage ( 'clone' ){
		      steps{
			       git "https://github.com/sirishamaddineni/guava"
		    }
		}
		stage ( 'complie' ){
		    steps{
		       withMaven( maven : 'Maven 3.5.2' ){
		       bat 'mvn clean compile'
		    }
		   }
		}
		stage ('testing' ){
		    steps{
		        withMaven( maven : 'Maven 3.5.2' ){
		        bat 'mvn test'
		       }
		    }
		}
   }
	
