1.	pipeline {
2.	    agent any
3.	 
4.	    tools {
5.	        maven 'localMaven'
6.	    }
7.	 
8.	stages{
9.	        stage('Build'){
10.	            steps {
11.	                sh 'mvn clean package'
                    echo 'Performing maven clean and package...'
12.	            }
13.	            post {
14.	                success {
15.	                    echo 'Now Archiving...'
16.	                    archiveArtifacts artifacts: '**/target/*.war'
17.	                }
18.	            }
19.	        }
20.	    }
21.	}
