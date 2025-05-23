// Jenkinsfile (Declarative Pipeline)
pipeline {
    agent any // Runs the pipeline on any available Jenkins agent (here, the Master itself)

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/my-simple-app.git' // Replace with your actual repository URL
            }
        }
        stage('Print Files') {
            steps {
                echo 'Listing files in workspace:'
                bat 'dir' // Use 'bat' for Windows commands
            }
        }
        stage('Cleanup') {
            steps {
                cleanWs() // Cleans the workspace after the build
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished!'
        }
        success {
            echo 'Build successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
