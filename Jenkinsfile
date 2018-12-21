	pipeline {
	    agent any
	 
	    tools {
	        maven 'MyLocalMaven'
	    }
	 
	stages{
	        stage('Build'){
	            steps {
	                sh 'mvn clean package'
                    echo 'Performing maven clean and package...'
               }
	            post {
	                success {
                    echo 'Now Archiving...'
	                    archiveArtifacts artifacts: '**/target/*.war'
	                }
	            }
	        }
	    }
	}
