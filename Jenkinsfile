pipeline{
    agent any
    parameters{
	string(defaultValue: 'us-east-2', name: 'awsRegion')
	string(name: 'keyname')
	string(name: 'values')
	string(name: 'documentname')
	string(name: 'awscredentialsId')
    }
	
    stages{
	stage('clear workspace'){
            steps{
	        sh 'echo "----------------- 1. Clears workspace -----------------"'
		deleteDir()
	    }
		
	}
	stage('build'){
	    steps{
	        sh 'echo "Building new instance"'
		withAWS(
		    credentials: "${params.awscredentialsId}",
                    region: "${params.awsRegion}"
	        ) {
	            script {
			    sh "aws ssm send-command --document-name ${params.documentname} --targets Key=tag:${params.keyname},Values=${params.value}"
		     }
			   
		   } 
		
	    }
	}    
        stage('cleanup'){
            steps{
		sh 'echo "cleaning up working space!!-->"'
		deleteDir() 
	    }
	}
    }	
}
