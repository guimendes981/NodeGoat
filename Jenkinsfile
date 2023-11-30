pipeline {
    agent any

    stages {
        stage('Testes') {
            steps {
                dir('/home/gui/Desktop/NodeGoat') {
                    sh 'sudo npm install' // Instalar dependências
                    sh 'sudo npm test'    // Executar os testes
                }
            }
        }
    }
}