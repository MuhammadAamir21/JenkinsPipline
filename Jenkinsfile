pipeline {
    agent any

      tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN_HOME"
    }

    stages {
        stage ('Build Stage') {

            steps {
               
                    bat 'mvn clean compile'
             
            }
        }

        stage ('Testing Stage') {

            steps {
              
                    bat 'mvn test'
              
            }
             post {
                always{
                    junit '**/target/surefile-reports/TEST-*.xml'
                }
            }
        }


    }
}