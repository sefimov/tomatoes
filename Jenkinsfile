pipeline {
    agent {
        node {
            docker { image 'registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest' }
        }
        
    }
    stages {
        stage('Test') {
            steps {
                sh 'bundle install'
                sh 'rake stats'
            }
        }
    }
}