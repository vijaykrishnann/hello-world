pipeline{
    agent any
    stages{
	stage("build'){
	    steps{
	        build(job: "abc", parameters:[
		string(name: 'org', value: 'Infy')
	        ])
	    }  
	}
    }	
}
