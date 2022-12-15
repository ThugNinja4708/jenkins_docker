
pipeline{
    agent any
    stages{
        stage('user input'){
            steps{
                script{
                    env.IMG = input message: 'Please enter the username',
                             parameters: [string(defaultValue: '',
                                          description: '',
                                          name: 'Username')]
        }
                IMAGE=${env.IMG} docker-compose up -d
                }
            }
        }
    }
