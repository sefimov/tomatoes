pipeline {
    agent none
    stages {
        stage ('n1') {
            environment {
                CHUTE_SERVICE_CI = credentials('test_c_text')
            }
            steps {
                sh "printenv"
            }
        }
    }
}
// pipeline {
//     agent none
    
//     stages {
//         /*stage("Build") {
//             agent {
//                 docker {
//                     image 'registry2.swarm.devfactory.com/chute/jenkins_agents/ruby_on_rails:latest'
//                 }
//             }
//             steps {
//                 sh 'bundle install'
//                 sh 'cap production deploy:check'
//                 sh 'cap production deploy'
//             }
//         }*/
//         stage('Test') {
//             agent any
//             environment {
//                 CHUTE_SERVICE_CI = credentials('chute_service_ci_credentials_id')
//             }
//             steps {
//                 sh 'echo $CHUTE_SERVICE_CI'
//                 sh 'echo $CHUTE_SERVICE_CI_USR'
//                 // also available as a Groovy variable
//                 sh 'echo $CHUTE_SERVICE_CI_PWD'
//             }
//         }
//     }
// }