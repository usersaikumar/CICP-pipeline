pipeline {

    agent any
  
    stages {
        stage("sonar Quality Check") {
                         
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