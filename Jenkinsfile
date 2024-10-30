pipeline {
  agent any 

   stages {
    stage('git checkout'){
        steps{
            git branch: 'main', url: 'https://github.com/terraform-devops34/aws-cicd.git'
        }
    }
    stage('test'){
        steps{
            sh 'echo test'
        }
    }
    stage('pwd command'){
        steps{
            sh 'pwd'
        }
    }
   }





}