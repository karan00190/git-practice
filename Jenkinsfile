// Jenkinsfile (Declarative Pipeline)
pipeline {
    agent any // Runs the pipeline on any available Jenkins agent (here, the Master itself)

    stages {
        // REMOVED THE PREVIOUS 'stage('Checkout')' HERE
        // The SCM checkout configured in the Jenkins job will handle getting the code.

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
