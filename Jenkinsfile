pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t app -f app/Dockerfile app'
            }
        }
        stage('Deploy') {
            steps {
                // Stop and remove any existing container named 'app'
                sh '''
                    docker stop app || true
                    docker rm app || true
                    docker run -d --name app -p 8080:80 app
                '''
            }
        }
    }
}
