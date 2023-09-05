pipeline {
  agent {
    docker {
      image 'node:18.17.1-alpine3.18'
      args '-p 3000:3000 '
    }

  }
  stages {
    stage('Welcome ') {
      steps {
        sh 'echo "coucou"'
      }
    }

    stage('installer ') {
      steps {
        sh 'npm install'
      }
    }

    stage('built') {
      steps {
        sh 'npm run build'
      }
    }

    stage('deploy') {
      steps {
        sh 'yarn global add firebase-tools'
      }
    }

  }
}