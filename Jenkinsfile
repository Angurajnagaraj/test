pipeline {
    agent any
    
    environment {
        GIT_REPO_URL = 'https://github.com/Angurajnagaraj/test'  // Your GitHub repository URL
        BRANCH_NAME = 'main'  // Branch you want to checkout, change as needed
        DOCKER_CREDENTIALS = credentials('DockerId')
    }

      stages {
        stage('Login to Docker Hub') {
            steps {
                script {
                    sh "echo \$DOCKER_CREDENTIALS_PSW | docker login -u \$DOCKER_CREDENTIALS_USR --password-stdin"
                }
            }
        }
	}
}
