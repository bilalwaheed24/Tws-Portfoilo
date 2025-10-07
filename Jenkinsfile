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
                echo 'No build needed for this static portfolio.'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    try {
                        echo '🚀 Deploying Portfolio to /var/www/html/'
                        sh '''
                            sudo cp -r * /var/www/html/
                            echo "✅ Deployment successful!"
                        '''
                    } catch (err) {
                        echo "❌ Deployment failed: ${err}"
                    }
                }
            }
        }
    }
}
