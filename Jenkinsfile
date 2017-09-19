pipeline {
	agent any
	
	
 	stages {
		stage('Build') {
			steps {
			//sh 'make'
				
			sh 'pwd'
			sh 'ls'
			sh 'cat README.md'
			echo 'Building ...'
		        sh 'printenv'
		  	}
		}

		stage ('Deploy PROD') {
			steps {
				timeout(time:1, unit:'DAYS'){
			        	input message: 'Are you sure ?'  	
					}
				input 'employing...'
			}
		}
	}	
}
