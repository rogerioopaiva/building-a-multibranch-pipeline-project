pipeline {
<<<<<<< HEAD
    agent {
       docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000'
        }
=======
  agent {
    docker {
      image 'node:12-alpine'
      args '-p 3000:3000 -p 5000:5000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
>>>>>>> 9b9e762f386e6b1eabf475c14c8b837c375573b1
    }

    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }

  }
  environment {
    CI = 'true'
  }
}