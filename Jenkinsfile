pipeline {
    agent {
        docker { image 'registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest' }   
    }
    stages {
        /*stage('Checkout GA') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: scm.branches,
                    doGenerateSubmoduleConfigurations: false,
                    extensions: scm.extensions + [[$class: 'SubmoduleOption', parentCredentials: true]],
                    userRemoteConfigs: scm.userRemoteConfigs
                ])
            }   
        }*/
        stage('Test') {
            steps {                
                sh 'ls'
                //sh 'rake stats'
            }
        }
    }
}