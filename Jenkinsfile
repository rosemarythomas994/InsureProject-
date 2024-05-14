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

   stage('publish test reports'){
     steps{
          publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: '/var/lib/jenkins/workspace/insureproject/target/surefire-reports', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])  
           }
         }
     
     }
}
         
