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
      
       stage('Build') {
				steps {
					script{
						sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml " 
					}
				}
			}
			 
			
	stage('docker') {
				steps {
					script{
						sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml " 
					}
				}
			}  
   	    
	 
  stage('docker-registry') {
				steps {
					script{
						sh "ansible-playbook ansible/docker-registry.yml -i ansible/inventory/host.yml " 
					}
				}
			}   
      
    }
}
