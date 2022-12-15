
pipeline{
    agent any
    stages{
        stage('user input'){
            steps{
                script{
                    env.IMAGE = input message: 'Please enter the username',
                             parameters: [string(defaultValue: 'nginx',
                                          description: '',
                                          name: 'Username')]
                }
            }
        }

        stage('launch container'){
            steps{
                sh '''
                echo ${env.IMAGE}
                IMAGE=${image} docker-compose up -d
                '''
            }
        }
    }
}
