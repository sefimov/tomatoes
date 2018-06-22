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
                sh 'export INT_STR=$(/sbin/ip route|cut -f3 -d" ")'
                sh 'export SERVER_IP=$( echo $INT_STR | cut -f1 -d" ")'
                sh 'echo $SERVER_IP'
                sh 'echo "$SERVER_IP generalhost" >> /etc/hosts'
                sh 'cap production deploy:check'
                sh 'cap production deploy'
            }
        }
    }
}