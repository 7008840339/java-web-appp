pipeline{
    agent {
        node {
            label 'jenkins-slave-node'
        }
    }
    stages {
        stage ('checkout code'){
            steps {
                git branch: 'main', url: 'https://github.com/7008840339/java-web-appp.git'
            }
        }
        stage ('build code'){
            steps{
                sh '/opt/maven/bin/mvn clean package'
            }
        }
     }
 }


