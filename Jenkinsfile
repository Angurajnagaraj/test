pipeline {
    agent any
    
    environment {
        GIT_REPO_URL = 'https://github.com/Angurajnagaraj/test'  // Your GitHub repository URL
        BRANCH_NAME = 'main'  // Branch you want to checkout, change as needed
        DOCKER_CREDENTIALS = credentials('DockerId')
    }

      stages {
       stage('Static Code Analysis') {
      environment {
        SONAR_URL = "http://localhost:9000"
      }
      steps {
        withCredentials([string(credentialsId: 'sonarqube', variable: 'SONAR_AUTH_TOKEN')]) {
          sh 'curl -I ${SONAR_URL}'
        }
      }
    }
	}
}
