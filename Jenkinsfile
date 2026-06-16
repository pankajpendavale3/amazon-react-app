pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/pankajpendavale3/amazon-react-app.git'
            }
        }

        stage('Build') {
            steps {
                dir('amazon-react-app') {
                    sh 'npm install'
                    sh 'npm run build'
                }
            }
        }
    }
}
