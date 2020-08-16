pipeline {
    agent any
      stages {
          stage('Upload to AWS') {
            steps{
              withAWS(credentials:'IDofAwsCredentials', region: 'us-west-2') {
                sh 'echo "Hello World!"'
                s3Upload(file:'index.html', bucket:'staticwebpvera02', path:'/index.html')
              }
            }
          }
      }
}
