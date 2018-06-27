pipeline {
    agent {
        node {
            label "chute-jenkins-ror"
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'bundle install'
                sh 'rake stats'
                sh 'docker version'
            }
        }
    }
}