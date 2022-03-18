pipeline {

    agent any

    tools {
      maven 'MAVEN'

    }

    
    stages {
        stage('Build Maven') {
            steps{
                 checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git_credentials', url: 'https://github.com/lakshmiKrishnaa/jenkins-maven.git']]])

                bat "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }
    }
    
}
