pipeline {
    agent any

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
        }


    }
}