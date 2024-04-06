pipeline {
    agent any
    
    stages {
        stage('checkout code') {
            steps {
                git branch: 'main', url: 'git_repo_url'
            }
        }
        stage('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
        stage('Deployment'){
			      steps{
				        deploy adapters: [ tomcat9(url: 'http://107.20.35.178:8080/', credentialsId: 'TomcatCreds')], war:'target/*.war'
			      }
		    }
    }
}
