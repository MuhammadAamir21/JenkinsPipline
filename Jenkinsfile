pipeline
 {
  agent any

  tools
   {
    maven 'MAVEN_HOME'
    jdk 'JAVA_HOME'
   }




  stages
   {
    

    stage('Build')
     {
      steps
       {
        script
         {
          if (isUnix()) 
           {
            sh 'mvn --batch-mode compile'
           }
          else
           {
            bat 'mvn --batch-mode compile'
           }
         }
       }
     }

    stage('UnitTests')
     {
      steps
       {
        script
         {
          if (isUnix()) 
           {
            sh 'mvn --batch-mode resources:testResources compiler:testCompile surefire:test'
           }
          else
           {
            bat 'mvn --batch-mode resources:testResources compiler:testCompile surefire:test'
           }
         }
       }
    
     }

   
 
    

   

  

   }

 }