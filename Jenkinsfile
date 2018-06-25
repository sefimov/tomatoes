pipeline {
    properties{
        promotion {
            conditions {
                manual('testuser')
            }
            actions {
                shell('echo hello;')
            }
        }
    }
    agent {
        docker {
            image('registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest')
        } 
    }
    stages {
        stage('Test') {
            steps {
                sh 'bundle install'
                sh 'cap production deploy:check'
                sh 'cap production deploy'
            }
        }
    }
}