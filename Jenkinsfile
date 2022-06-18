pipeline{

    agent any
  
    stages{
        stage("sonar quality Check"){
            agent{
                docker{
                    image 'openjdk:11'
                }
            }
            steps{
               script{
                withSonarQubeEnv(credentialsId: 'sonar-token'){
                        sh 'chmod +X gradlew'
                        sh './gradlew sonarqube'
                    }

               }
            }
          
        }
    }
}
