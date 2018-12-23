pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
			bat
				 'cd c:\\git\\repos\\maven-project'
                 'mvn clean package'
            }
            post {
                success {
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}