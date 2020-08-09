pipeline {
  agent any
  stages{
    stage ('Create AWS Stack') {
      steps {
        echo "Creating AWS CloudFormation Stack"
        withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'aws-key', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
       sh 'aws cloudformation create-stack --stack-name petclinic --template-body file://aws-template-petclinic.yaml --region us-east-1 --parameters  ParameterKey=SSHKey,ParameterValue=devops ParameterKey=ELBVPC,ParameterValue=vpc-934dbbee ParameterKey=ELBSubnet,ParameterValue="subnet-fe7099cf\\,subnet-278e2e06"'
        }      
      }
    }
  }
}
