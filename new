pipeline {
     agent {
	   node {
	    label 'slave1' 
		  customWorkspace '/mnt/demo'
	 }
	 }
	 parameters {
	       choice(name: 'ENV', choices: ['stage', 'dev'], description: '')
		   }
		   
		   stages {
		      stage ('example') {
			      steps {
				       sh '''if [ ENV = stage ]
					   then
					   echo "these is staging"
					   else
					   echo "tis is dev" 
					   fi'''
					   }
		   }
	   }
	   }
