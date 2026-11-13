
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Sreedev895/python.git'
            }
        }

        stage('Deploy Django Application') {
            steps {
                sh '''
                    cd /home/ubuntu/python_docker
                    git pull origin main
                    docker compose build
                    docker compose up -d
                '''
            }
        }
    }
}
