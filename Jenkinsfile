
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
                echo "${env.IMG}"

                }
            
            }
        stage("build docker compose "){
            steps{
                sh """
                    pwd
                    sudo IMAGE=${env.IMG} docker-compose up -d
                """
            
                }
        
            }
        }
    }
