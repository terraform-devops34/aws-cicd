pipeline {
  agent any 

  environment {
    BRANCH_NAME = 'main'
    GTI_URL =  'https://github.com/terraform-devops34/aws-cicd.git'
  }

   stages {
    stage('git checkout'){
        steps{
            git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
    }  
    stage('docker build'){
        steps{
            sh 'docker build -t aws-cicd .'
            sh 'docker images'
        }
    }
    stage('pwd command'){
        steps{
            sh 'pwd'
        }
    }
   }





}