pipeline{
    agent any
    stages{
        stage("verify tooling"){
            steps{
                sh '''
                docker version
                docker info
                dcoker compose version
                curl --version  
                '''
            }
        }
    }
}
