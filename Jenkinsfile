pipeline {
    agent none
    stages {
        stage('Test') {
            agent {
                label "chute-jenkins-ror"
            }
            steps {
                sh 'bundle install'
                sh 'rake stats'
            }
        }
    }
}