   pipeline
   {

		agent any
		  stages {
		      stage('Pull') {
			   steps{
			      script{
				  checkout([$class: 'GitSCM', branches: [[name: '*/master']],
				      userRemoteConfigs: [[
					  credentialsId: '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',
					  url: 'https://github.com/BJyoussef/myCDproject.git']]])
			      }
		          }
		          }
		          
		          
		      stage('build') { 
		           steps{
			      script{
				sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml"
			      		}
		          	}
		     		}
	     
	     
		      stage('Docker') {
		           steps{
                              script{
                                sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml"
                                }
                          }
                     }
                     
                     
                     stage('Docker-Registry') {
                           steps{
                              script{
                                sh "ansible-playbook ansible/docker-registry.yml -i ansible/inventory/host.yml"
                                }
                          }
                     }
                     
	     
	     }
	     
	     
	     }

