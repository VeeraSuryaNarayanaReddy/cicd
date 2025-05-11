pipeline{
    agent any
    stages{
        stage('Build and deploy'){
            steps{
                sh 'docker build -t app -f /app/Dockerfile'
            }
        }
    }
}