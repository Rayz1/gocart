pipeline {
    agent any 
 tools {
    nodejs "node-js24"
 }  	   


    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout…'
                echo 'Source code checkout from Git (handeled by…'
            }
        }

        stage('Install dependencies') {
            steps {
                echo 'Installing npm dependencies…'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing…'
            }
        }

        stage('Run_dev') {
            steps {
                echo 'Runing npm dev…'
                sh 'npm run dev'
            }
        }
    }

    post {
        success {
            echo 'Success…'
            echo 'Send status Success to Mail, Telegram, Slack…'
        }
        failure {
            echo 'Failure…'
            echo 'Send status Failure to Mail, Telegram, Slack…'
        }
    }
}
