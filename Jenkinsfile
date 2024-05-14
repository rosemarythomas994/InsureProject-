pipeline {
  agent any

  tools {
    maven 'M2_HOME'
    }
  
  stages {
    stage('CheckOut') {
      steps {
        echo 'Checkout the source code from GitHub'
        git branch: 'main', url: 'https://github.com/rosemarythomas994/InsureProject-.git'
            }
    } 
    stage('package'){
      steps{
        echo 'Create a package'
        sh 'mvn clean package'
           }
        }
    }
}
         
