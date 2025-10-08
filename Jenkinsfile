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
                script {
                    try {
                        echo '🚀 Deploying Portfolio to /var/www/html/ ...'

                        // Copy all files to deployment folder
                        sh '''
                            cp -r * /var/www/html/
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
