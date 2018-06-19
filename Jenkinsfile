pipeline {
    agent {
        node('docker_agent') {
            docker.image('registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest')
                .inside {
                    rvm 'bundle install' 
                    rvm 'bundle exec rake stat'
                }
        } 
    }
    stages {
        stage('Test') {
            steps {                
                sh 'ls'
            }
        }
    }
}