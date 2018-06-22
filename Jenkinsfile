pipeline {
    agent {
        docker {
            image('registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest')
        } 
    }
    stages {
        stage('Test') {
            steps {
                sh 'export SERVER_IP=172.18.0.1'
                sh 'echo $SERVER_IP'
                sh 'bundle install'
                sh 'echo "$SERVER_IP generalhost" >> /etc/hosts'
                sh 'cap production deploy:check'
                sh 'cap production deploy'
            }
        }
    }
}