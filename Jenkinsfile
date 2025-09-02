pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo '📦 Downloading code from GitHub...'
            }
        }
        
        stage('List Files') {
            steps {
                echo '📁 Listing HTML files...'
                bat 'dir *.html'
            }
        }
        
        stage('Success Message') {
            steps {
                echo '🎉 All stages completed successfully!'
                bat 'echo "Your site is ready for deployment!"'
            }
        }
    }
    
    post {
        always {
            echo '🏁 Pipeline execution finished'
        }
    }
}
