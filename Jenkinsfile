pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                retry(3){
                    withAWS(region:'us-east-2', credentials:'Jenkins') {
                    s3Upload(file:'index.html', bucket:'jenkins-jokoss92', path:'')
                }
              }
            }
        }
    }
}