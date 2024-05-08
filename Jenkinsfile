pipeline{
  agent any
  stages{
    stage('S3'){
      steps{
         withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', credentialsId: 'AWS_ID']]) {
                    sh "/usr/bin/aws s3 rm  s3://test-ui-command/assets/videos/ --recursive"
        }
      }
    }
  }
}
