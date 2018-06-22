pipeline {
    agent {
        docker {
            image('registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest')
        } 
    }
    stages {
        stage('Test') {
            steps {
                sh 'bundle install'
                sh "export SERVER_IP=$(/sbin/ip route|awk '/default/ { print $3 }')"
                sh 'echo $SERVER_IP'
                sh 'echo "$SERVER_IP generalhost" >> /etc/hosts'
                sh 'cap production deploy:check'
                sh 'cap production deploy'
            }
        }
    }
}