pipeline{
    agent any
	stages{
	    stage("build"){
		steps{
	            echo "Hello ${params.org}"
		    sh "aws ssm send-command --targets "Key=tag:${params.keyname},Values=${params.values}" --document-name "{params.documentname}" --profile ${params.env}"
		      }
	    }    
            stage("cleanup"){
		steps{
		    echo "cleaning up working space!!"
		    deleteDir() 
	             }
	    }
	}	
}
