pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/bilalwaheed24/Tws-Portfoilo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'No build needed — static website project'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Portfolio...'
                sh '''
                rm -rf /var/www/html/*
                cp -r * /var/www/html/
                '''
            }
        }
    }

    post {
        success {
            echo '🎉 Portfolio deployed successfully!'
        }
        failure {
            echo '❌ Deployment failed!'
        }
    }
}
