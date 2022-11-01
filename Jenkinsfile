pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                        userRemoteConfigs: [[
                            credentialsId: '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',
                            url: 'https://github.com/rim-bdiwi/Angular.git']]])
                }
            }
        }
