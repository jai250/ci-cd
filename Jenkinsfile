pipeline {
    agent any
    stages {
        stage("CHECKOUT code") {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/jai250/ci-cd.git',
                        credentialsId: 'your-credentials-id'
                    ]]
                ])
            }
        }
        stage("check") {
            steps {
                sh '''
                   pwd
                   ls -lrta
                '''
            }
        }
    }
}  