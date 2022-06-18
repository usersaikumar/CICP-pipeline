pipeline {

    agent any
  
    stages {
        stage("sonar Quality Check") {
            agent {
                docker {
                    image 'maven'
                }
            }
            steps {
               script {
                withSonarQubeEnv(credentialsId: 'sonar-token') {
                        sh 'chmod +X gradlew'
                        sh './gradlew sonarqube'
                    }

               }
            }
          
        }
    }
}