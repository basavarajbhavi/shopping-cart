pipeline {
  agent any
  stages{
    stage ('Create AWS Stack') {
      steps {
        echo "Creating AWS CloudFormation Stack"
        withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'aws-key', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
       sh 'aws s3 ls'
        }      
      }
    }
  }
}
