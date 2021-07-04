pipeline {
    agent any

      tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN_HOME"
    }

    stages {
        stage ('Build Stage') {

            steps {
                   git 'https://github.com/MuhammadAamir21/JenkinsPipline.git'
                    bat 'mvn clean compile'
             
            }
        }

        stage ('Testing Stage') {

            steps {
              git 'https://github.com/MuhammadAamir21/JenkinsPipline.git'
                  bat 'mvn --batch-mode resources:test compiler:testCompile surefire:test'
              
            }
             post {
                always{
                   junit '**/target/surefire-reports/TEST-*.xml'
                   archiveArtifacts 'target/*.jar'
                }
            }
        }


    }
}