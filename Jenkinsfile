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
	     }
	     }

