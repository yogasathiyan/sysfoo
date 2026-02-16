pipeline {
  agent any
  tools{
    maven 'maven 3.9.12'
  }
  stages{
    stage("build"){
        steps{
        echo 'step 1-compiling'
        sh 'mvn compile'
        }
    }
        stage("test"){
            steps{
              echo 'step 2-test'
            sh 'mvn clean test'
            
        }
    }
    stage("package"){
         steps{
         echo 'step 3-package'
         sh 'mvn package -DskipTests'
        }
    }
 }
    post{
        always{
        echo 'This pipeline is completed..'
        }
    }
}
