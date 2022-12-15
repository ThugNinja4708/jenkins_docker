
pipeline{
    agent any
    stages{
        stage('user input'){
            steps{
                script{
                    env.USERNAME = input message: 'Please enter the username',
                             parameters: [string(defaultValue: '',
                                          description: '',
                                          name: 'Username')]
        }
                IMAGE=${env.USERNAME} docker-compose up -d
                }
            }
        }
    }
