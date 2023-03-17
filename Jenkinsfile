pipeline {
  agent any
  environment {
    AWS_DEFAULT_REGION="ap-south-1"
}
  stages {
    stage ('Hello All') {
        steps {
            withCredentials([aws(accessKeyVariable:'AWS_ACCESS_KEY_ID',credentialsId:'ec2user',secretKeyVariable:'AWS_SECRET_ACCESS_KEY')]){
            sh '''
            aws --version
            aws ec2 start-instances --instance-ids i-0154f303c114eb4cc
             '''
             }
          }
       }
   }
}
