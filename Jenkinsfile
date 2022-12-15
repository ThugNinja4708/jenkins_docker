pipeline{
    agent any
    stages{
        stage("verify tooling"){
            steps{
                sh '''
                IMAGE=$(params.IMAGE) docker-compose up -d
                '''
            }
        }
    }
}
