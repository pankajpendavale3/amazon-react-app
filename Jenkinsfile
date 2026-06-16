pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/pankajpendavale3/amazon-react-app.git'
            }
        }

        stage('Debug') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                sh 'find . -name package.json'
            }
        }
    }
}
