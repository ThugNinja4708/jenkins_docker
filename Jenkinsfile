pipeline{
    agent any
    stages{
        stage("verify tooling"){
            steps{
                sh '''
                sudo service docker start
                docker version
                docker info
                dcoker compose version
                curl --version  
                '''
            }
        }
    }
}