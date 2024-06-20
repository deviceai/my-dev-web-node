pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/deviceai/my-dev-web-node.git', branch: 'main')
      }
    }

    stage('Log') {
      parallel {
        stage('Log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('cd frontend') {
          steps {
            sh 'cd frontend'
          }
        }

      }
    }

    stage('Docker build') {
      steps {
        sh 'docker build -f frontend/Dockerfile .'
      }
    }

  }
}