pipeline {
    agent none
    stages {
        /*stage("Build") {
            agent {
                docker {
                    image 'registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest'
                }
            }
            steps {
                sh 'bundle install'
                sh 'cap production deploy:check'
                sh 'cap production deploy'
            }
        }*/
        stage('Test') {
            agent any
            steps {
                sh 'echo $(git rev-parse --short HEAD)'
            }
        }
    }
}