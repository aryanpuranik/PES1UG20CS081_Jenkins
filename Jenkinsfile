pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ -o cs160 cs160.cpp'
        build job: 'PES1UG20CS160-1'
        echo "BUILD successful"
      }
    }
    stage('Test') {
      steps {
        sh './cs160'
        echo "TEST successful"
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deployment stage"'
        sh 'exit 1'
        echo "DEPLOY successful"
      }
    }
  }

  post {
    failure {
     echo 'Pipeline failed.'
    }
  }
}
