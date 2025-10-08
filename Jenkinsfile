pipeline {
    agent any
    
    stages {

        stage('Checkout') {
            steps {
                echo "Fetching source code from GitHub..."
                git branch: 'main', url: 'https://github.com/NahidCSERU/nodejs-socketio-chat-application.git'
            }
        }


        stage('Build Docker image') {
            steps {
                echo 'Building Docker socketio image...'
                sh 'docker build -t socketio .'
            }
        }
        stage('Run Docker Container for socketio') {
            steps {
                echo 'Running Docker container...'
                sh 'docker run -d -p 3000:3000 --name socketio_container socketio'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy steps here
            }
        }
    }

    post {
        always {
            echo 'This will always run after the stages.'
        }
        success {
            echo 'This will run only if the pipeline succeeds.'
        }
        failure {
            echo 'This will run only if the pipeline fails.'
        }
    }
}