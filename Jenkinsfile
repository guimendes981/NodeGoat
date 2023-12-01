

pipeline{

    agent any

    environment {
    CYPRESS_CACHE_FOLDER = "$WORKSPACE/cypress_cache"
}

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
                    sudo docker build .
                '''
            }
        }
        stage('Compose Docker') {
            steps {
                sh '''
                   sudo docker compose up
                '''
            }
        }
    }
}