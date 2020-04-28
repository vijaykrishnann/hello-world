pipeline{
    agent any
	stages{
	    stage("build"){
		steps{
	            echo "Hello ${params.org}"
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
