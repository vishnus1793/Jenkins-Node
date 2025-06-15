pipeline {
  agent {
    node {
      label 'Node'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/vishnus1793/Jenkins-Node'
      }
    }

    stage('Install') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'npx jest'
      }
    }

    stage('Deploy') {
      steps {
        sh 'node index.js &'
      }
    }

  }
}