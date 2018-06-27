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
        stage('Build docker') {
            agent {
                label "optiva"
            }
            steps {
                sh 'docker version'
            }
        }
    }
}