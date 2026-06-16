pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/pankajpendavale3/amazon-react-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test -- --watchAll=false'
            }
        }

        stage('Package') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo rm -rf /var/www/html/*
                sudo cp -r build/* /var/www/html/
                '''
            }
        }
    }
}
