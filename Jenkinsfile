pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ -o cs081 cs081.cpp'
        build job: 'PES1UG20CS081-1'
        echo "BUILD successful"
      }
    }
    stage('Test') {
      steps {
        sh './cs081'
        echo "TEST successful"
      }
    }
    stage('Deploy') {
      steps {
//         sh 'echo "Deployment stage"'
//         sh 'exit 1'
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
