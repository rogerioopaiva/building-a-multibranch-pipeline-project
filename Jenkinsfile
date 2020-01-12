pipeline {
    agent {
        docker {
            image 'node6-alpine'
            args '-p 3000:3000 -p 5000:5000'
        }
    }
    enviroment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}