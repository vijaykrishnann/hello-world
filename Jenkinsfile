pipeline{
    agent any
    stages{
	stage("build"){
	    steps{
	        build(job: "abc", parameters:[
		string(name: 'org', value: 'Infy'),
		string(name: 'keyname', value: 'Name'),
		string(name: 'values', value: 'Terraform')
		string(name: 'documentname', value: 'terraform'),
		string(name: 'awscredentialsId', value: 'aws_automation')
	        ])
	    }  
	}
    }	
}
