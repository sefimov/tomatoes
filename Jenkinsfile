pipeline {
    agent {
        docker {
            image('registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest')
        } 
    }
    stages {
        stage('Test') {
            steps {
                sh "whoami"
                sh "chmod -R 777 /usr/local/bundle/cache/"                
                sh "ls && bundle install"
            }
        }
    }
}