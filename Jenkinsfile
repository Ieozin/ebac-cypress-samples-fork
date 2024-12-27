pipeline {
    agent any

    stages {
        stage('Clonar o Repositório') {
            steps {
                git(branch: 'main', url: 'https://github.com/Ieozin/ebac-cypress-samples-fork.git')
            }
        }
        stage('Instalar Dependências') {
            steps {
                bat 'npm install'
            }
        }
        stage('Executar Testes') {
            steps {
                bat 'set NO_COLOR=1 && npm run test'
            }
        }
    }
}
