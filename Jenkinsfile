pipeline {
    agent any
    
    environment {
        GIT_REPO_URL = 'https://github.com/Angurajnagaraj/Jenkins-Zero-To-Hero'  // Your GitHub repository URL
        BRANCH_NAME = 'main'  // Branch you want to checkout, change as needed
    }

    stages {
        stage('Checkout Code') {
            steps {
                script {
                    // Checkout the code from GitHub
                    git url: "${GIT_REPO_URL}", branch: "${BRANCH_NAME}"
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                sh '''pwd
                    cat hello.py'''
                // Add build steps here (e.g., Maven, Gradle, etc.)
            }
        }

        // Add more stages as necessary (e.g., Test, Deploy)
    }

    post {
        always {
            echo 'Cleaning up after the build...'
            // You can clean up resources or perform post-build actions here
        }
    }
}
