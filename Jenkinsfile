pipeline {
agent any stages {
stage('Build') { steps {
sh 'g++ -o cs081 cs081.cpp' }
} stage('Test') {
steps {
sh './cs081'
} }
stage('Deploy') { steps {
echo 'deployed successfully' }
} }
post { always {
script {
if (currentBuild.result == 'FAILURE') {
echo 'pipeline failed' }
} }
} }
