pipeline {
    agent {
        docker {
            image('registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest')
            // args '-u root:sudo'
        } 
    }
    stages {
        stage('Test') {
            steps {
                // sh 'chmod -R 777 /usr/local/bundle/cache/'
                sh 'ls && bundle install'
                sh 'rake stats'
            }
        }
    }
}