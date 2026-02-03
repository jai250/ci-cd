pipeline {
    agent any
    stages {
        stage("CHECKOUT code") {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/jai250/shell-scripting-personal.git',
                        
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