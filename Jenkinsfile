pipeline {

    agent any
  
    stages {
        stage("sonar Quality Check") {
            agent {
                docker {
                    image 'openjdk:8'
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