pipeline {
    agent any
    
    stages {
        stage('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/7008840339/java-web-appp.git'
            }
        }
        stage('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
        stage('Deployment'){
	   steps{
		deploy adapters: [ tomcat9(url: 'http://50.18.98.178:8080/', credentialsId: 'tomcatcred')], war:'target/*.war'
	   }
	}
    }
}
