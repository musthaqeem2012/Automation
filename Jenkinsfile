#!/usr/bin/env groovy
pipeline {
    

 parameters {
    //string(defaultValue: "TEST", description: 'What environment?', name: 'userFlag')
    choice(choices: ['DEV', 'STAGING', 'PRODUCTION'], description: 'Select field for target environment', name: 'DEPLOY_ENV')
    }
    agent any

    stages {
       /*stage('Scm') {
            steps {
                echo 'Building..'
		
				
                sh 'mvn --version'
                 git 'https://github.com/musthaqeem2012/simple-app.git'
                 
            }
        }*/
       
		
	
       stage('Deploy to Dev') {
		when {
                branch 'development'
           	 }
           	 steps {
		     
                echo 'Deploying....'
             	    
                sh "pwd"
		
                echo 'Deployed Successfully in DEV'
            
		     }
	    
        }
		
       stage('Deploy to Prod') {
		/*when {
                branch 'production'
           	 }	*/
           	 steps {
		     
                echo 'Deploying....'
             	    
                sh "pwd"
		
                echo 'Deployed Successfully in production'
            
		     }
	    
        }		        
    }
}
