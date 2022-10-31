pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[
                            credentialsId: 'b7e208e2-187c-4d10-930d-954dbd2f2ead',
                            url: 'https://github.com/rim-bdiwi/Angular.git']]])
                }
            }
        }
