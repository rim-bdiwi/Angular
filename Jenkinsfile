pipeline 
{
    agent any
    stages {
  
        stage('pull') {
            steps{
              script{
                checkout([&class: 'GITSCM', branches: [[name: '*/master']],
                          userRemoteConfigs: [[
                            credentialsId: '',
                            url: 'https://github.com/rim-bdiwi/Angular/new/main']]])
            }
        }
    }
}
}
