

pipeline{

    agent any

    environment {
    CYPRESS_CACHE_FOLDER = "$WORKSPACE/cypress_cache"
}

    stages {
        stage('Install NPM') {
            steps {
                sh '''
                    npm install
                '''
            }
        }
        stage('Test NPM') {
            steps {
                sh '''
                     npm test
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