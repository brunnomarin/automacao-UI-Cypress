pipeline {
    agent any
    options {
        ansiColor('xterm')
    }

    stages {
        stage('Clonar Repositório') {
            steps {
                git branch: 'main', url: 'https://github.com/brunnomarin/automacao-UI-Cypress.git'
            }
        }

        stage ('Instalar Dependências') {
            steps {
                bat 'npm install --force'
            }
        }
        
       stage ('Executar Testes') {
            steps {
                bat 'npm run cy:run'
            }
        }

    }

}