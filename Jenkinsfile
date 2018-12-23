	pipeline {
	    agent any
	 
	    tools {
	        maven 'MyLocalMaven'
	    }
	 
	stages{
			stage('Initialize'){
	            steps {
					sh 'cd /c/git/repos/maven-project'
	            }
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
