def image = null
pipeline{
    agent any
    stages{
        stage('user input'){
            steps{
                script{
                    image = input(
                        messgae: 'enter the image name',
                        ok: 'Submit',
                        parameters: [string(defaultValue: 'nginx', name: 'image name')]
                    )
                }
            }
        }

        stage('launch container'){
            steps{
                sh '''
                IMAGE=${image} docker-compose up -d
                '''
            }
        }
    }
}
