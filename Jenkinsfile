pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
			bat
				 'mvn -f c:\\git\\repos\\maven-project clean package'
            }
            post {
                success {
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}