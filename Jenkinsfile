pipeline {
    agent any
    stages {
        stage ('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
         withAWS(credentials: 'aws static', region: 'us-east-1') {

            s3Upload(bucket:'elmokdad-jenkins-udacity',file:'Index.html')

                }
            }
        }
    }
}
