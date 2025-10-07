pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/bilalwaheed24/Tws-Portfoilo.git'
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
                # Example: copy files to /var/www/html/
                sudo rm -rf /var/www/html/*
                sudo cp -r * /var/www/html/
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
