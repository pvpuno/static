pipeline {
    agent any
      stages {
          stage('Upload to AWS') {
            steps{
              withAWS(credentials:'jenkins', region: 'us-west-2') {
                s3Upload(file:'index.html', bucket:'staticwebpvera02', path:'/index.html')
              }
              sh 'echo "Hello World!"'
            }
          }
      }
}
