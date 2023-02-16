pipeline {
agent any

stages {
stage('Build') {
steps {
sh 'g++ -o CS081_Aryan CS081_Aryan.cpp'
}
}
stage('Test') {
steps {
sh './CS081_Aryan'
build job: 'PES1UG20CS081-1'
}
}
stage('Deploy') {
steps {
sh 'echo "Deployment stage"'
sh 'exit 1'

}
}
}

post {
always {
echo 'Pipeline completed.'
}

failure {
echo 'Pipeline failed.'
}
}
}
