 node ('any'){
        stage('checkout code') {
                git branch: 'main', url: 'https://github.com/7008840339/java-web-appp.git'
        }
        
        stage('build code') {
                sh '/opt/maven/bin/mvn clean package'
        }
        
        stage('Deployment'){
		deploy adapters: [ tomcat9(url: 'http://50.18.98.178:8080/', credentialsId: 'tomcatcred')], war:'target/*.war'
	}
}
    

