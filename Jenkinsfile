pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                git url: 'https://github.com/akshatluthra/DevOps-Two-Tier-App.git', branch: 'main'
            }
        }

        stage('Build'){
            steps{
                sh '''
                    sudo apt-get update
                    sudo apt-get install -y docker.io
                    docker --version
                   '''
            }
        }

        stage('Run'){
            steps{
                sh '''
                    docker run -d -p 8080:80 myapp:v1
                    '''
            }
        }
    }
}
