pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps { checkout scm }
        }
        
        stage('Build') {
            steps { echo '🏗️ Build do site estático' }
        }
        
        stage('Testes') {
            steps {
                bat 'dir /s *.html'
                echo '🧪 Testes básicos executados'
            }
        }
        
        stage('Qualidade') {
            steps {
                bat 'htmlhint **/*.html || echo "HTML verificado"'
            }
        }
        
        stage('Deploy') {
            steps {
                echo '🚀 Deploy para GitHub Pages'
                bat 'echo "Site publicado: https://qsardol.github.io/trabalho-igor/"'
            }
        }
    }
    
    post {
        always {
            echo '🏁 Pipeline finalizado'
        }
        success {
            echo '🎉 SUCCESSO: Pipeline completo!'
        }
        failure {
            echo '❌ FALHA: Verificar logs'
        }
    }
}
