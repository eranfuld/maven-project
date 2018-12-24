pipeline {
    agent any
	tools {
        maven 'MyLocalMaven'
		jdk 'MyLocalJDK'
    }
    stages{
        stage('Build'){
			
            steps {
				
			bat 'mvn -f c:\\git\\repos\\maven-project clean package'
            }
            post {
                success {
                    archiveArtifacts artifacts: 'C:\\git\\repos\\maven-project\\webapp\\target\\*.war'
                }
            }
        }
    }
}