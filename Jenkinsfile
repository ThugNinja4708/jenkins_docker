pipeline{
    agent any
    stages{
        stage("verify tooling"){
            steps{
                sh '''
                IMAGE=$(params.image) docker-compose up -d
                '''
            }
        }
    }
}
