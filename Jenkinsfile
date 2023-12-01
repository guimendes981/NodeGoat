

pipeline{

    agent any

    stages {
        stage('Sudo') {
            steps {
                sh '''
                    sudo su
                '''
            }
        }
        stage('Install NPM') {
            steps {
                sh '''
                    sudo npm install
                '''
            }
        }
        stage('Test NPM') {
            steps {
                sh '''
                    sudo npm test
                '''
            }
        }
        stage('Construindo Docker') {
            steps {
                sh '''
                    docker build .
                '''
            }
        }
        stage('Compose Docker') {
            steps {
                sh '''
                    docker compose up
                '''
            }
        }
    }
}