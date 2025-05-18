pipeline {
  agent any 

  environment {
    BRANCH_NAME = 'main'
    GTI_URL =  'https://github.com/terraform-devops34/aws-cicd.git'
    IMAGE_TAG = 'terraform-devops34/aws-cicd'
    IMAGE_VERSION = "${BUILD_NUMBER}"
  }

   stages {
    stage('git checkout'){
        steps{
            git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
        }
    }  
    stage('docker build'){
        steps{
            sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}"  .'
            sh 'docker images'
        }
    }
    stage('pwd command'){
        steps{
            sh 'pwd'
        }
    }
    stage('ls command'){
        steps{
            sh 'ls -l'
        }
    }
    stage('os command'){
        steps{
            sh 'uname -a'
        }
    }
   }





}