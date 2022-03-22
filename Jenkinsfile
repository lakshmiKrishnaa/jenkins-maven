pipeline {

    agent any

    tools {
      maven 'MVN'

    }

    
    stages {
        stage('Build Maven') {
            steps{
               bat "git clone  https://github.com/lakshmiKrishnaa/jenkins-maven.git"

                bat "mvn -Dmaven.test.failure.ignore=true clean package -f jenkins-maven"
                
            }
        }
    }
    
}
