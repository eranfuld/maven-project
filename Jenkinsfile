	pipeline {
	    agent any
	 
	    tools {
	        maven 'MyLocalMaven'
	    }
	 
	stages{
	        stage('Build'){
	            steps {
					cd c:\git\repos\maven-project
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
