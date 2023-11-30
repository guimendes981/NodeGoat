pipeline {
    agent any

    stages {
        stage('Testes') {
            steps {
                dir('/home/gui/Desktop/NodeGoat') {
                    sh 'npm install' // Instalar dependências
                    sh 'npm test'    // Executar os testes
                }
            }
        }
    }
}