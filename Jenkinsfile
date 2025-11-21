pipeline {
    agent any 
 tools {
    nodejs "node-js24"
 }  	   

    stages {
        stage('Checkout') {
            steps {
                echo "Source code checkout from Git (handled by Jenkins SCM…)"
            }
        }

        stage('Install dependencies') {
            steps {
                echo "Installing npm dependencies…"
                sh 'npm install'
            }
        }

        stage('Run_dev') {
            steps {
                echo "Running npm dev…"
                sh 'npm run dev &'
            }
        }
    }

    post {
        success {
            echo "Send status Success to Mail, Telegram, Slack…"
        }
        failure {
            echo "Send status Failure to Mail, Telegram, Slack…"
        }
    }
}
