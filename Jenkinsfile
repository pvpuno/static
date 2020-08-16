pipeline {
    agent any
      stages {
          stage('Upload to AWS') {
              withAWS(credentials:'IDofAwsCredentials', region: 'us-west-2') {
              sh 'echo "Hello World!"'
              s3Upload(file:'index.html', bucket:'staticwebpvera02', path:'/index.html')
            }
          }
      }
}
