pipeline {
    agent none
    stages {
        stage('Test') {
            node {
                label "chute-jenkins-ror"
            }
            steps {
                sh 'bundle install'
                sh 'rake stats'
            }
        }
    }
}