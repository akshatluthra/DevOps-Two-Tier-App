pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                git url: 'https://github.com/akshatluthra/DevOps-Two-Tier-App.git' branch: 'main'
            }
        }

        stage('Build'){
            steps{
                sh '''
                    docker build -t myapp:v1 .
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
