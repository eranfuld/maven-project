pipeline {
    agent any
    stages{
        stage('Build'){
			
            steps {
				withMaven(
        // Maven installation declared in the Jenkins "Global Tool Configuration"
        maven: 'M3',
        // Maven settings.xml file defined with the Jenkins Config File Provider Plugin
        // Maven settings and global settings can also be defined in Jenkins Global Tools Configuration
        mavenSettingsConfig: 'MyLocalMaven',
        mavenLocalRepo: '.repository') {
			bat 'mvn -f c:\\git\\repos\\maven-project clean package'
			}
            }
            post {
                success {
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}