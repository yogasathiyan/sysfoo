pipeline {
  agent any
  tools{
    maven 'maven 3.9.12'
  }
  stages{
    stage("build"){
        steps{
        echo 'step 1-compiling'
        bat 'mvn compile'
        }
    }
        stage("test"){
            steps{
              echo 'step 2-test'
            bat 'mvn clean test'
            
        }
    }
    stage("package"){
         steps{
         echo 'step 3-package'
         bat 'mvn package -DskipTests'
        }
    }
 }
    post{
        always{
        echo 'This pipeline is completed..'
        }
    }
}
