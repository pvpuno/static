pipeline {
    agent any
      stages {
          stage('Upload to AWS') {
            steps{
              withAWS(credentials:'aws-static', region: 'us-west-2') {
                s3Upload(file:'*.html', bucket:'staticwebpvera02', path:'index.html')
              }
              sh 'echo "Hello World!"'
            }
          }
      }
}
