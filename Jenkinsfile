pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo '📦 Baixando código...'
            }
        }
        
        stage('Validar HTML') {
            steps {
                echo '🔍 Verificando arquivos HTML...'
                bat 'dir *.html'
            }
        }
        
        stage('Deploy Simulado') {
            steps {
                echo '🚀 Preparando para deploy...'
                bat 'echo "Site pronto para ser publicado!"'
            }
        }
    }
    
    post {
        success {
            echo '🎉 Pipeline executado com sucesso!'
        }
    }
}
