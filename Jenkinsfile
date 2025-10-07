pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Option 1 (recommended)
                git branch: 'main', url: 'https://github.com/bilalwaheed24/Tws-Portfoilo.git'

                // Option 2 (if Git is already set in Jenkins job)
                // checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'No build needed — static website project'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    try {
                        echo '🚀 Deploying Portfolio...'
                        sh '''
                            sudo cp -r * /var/www/html/
                            echo "✅ Deployment completed successfully!"
                        '''
                    } catch (err) {
                        echo '❌ Deployment failed!'
                        error("Deployment step failed: ${err}")
                    }
                }
            }
        }
    }
}
