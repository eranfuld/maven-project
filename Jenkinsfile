	pipeline {
	    agent any
	 
	    tools {
	        maven 'MyLocalMaven'
	    }
	 
	stages{
	        stage('Build'){
	            steps {
	                sh 'mvn clean package'
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
