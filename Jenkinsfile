pipeline{
    agent any
	stages{
	    stage("gitcheckout"){
		steps{
		    echo "helloworld"
		     }
	    }
	    stage("second step"){
		steps{
		    echo "f**k off !!!!"
		     }
	    }
	    stage("cleanup"){
		    steps{
		        echo "cleaning up working space"
			deleteDir()   
		    }
	    }
	}

}
