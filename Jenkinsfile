pipeline {
	agent any
	
	environment {
		GLOBAL_VAR = 'My Global Var'
		}
	parameters {
		string(name: 'DEPLOYER', defaultValue: 'Mr Jenkins', description: 'who are you ?')
		choice(name: 'DEPLOY_TO', choices: 'development/nproduction', description: 'Deploy to ...')
	}

	
	triggers {
		pollSCM('* * * * *')
		}
	
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
		stage ('Test') {
			steps{
			//sh 'make check'
			//junit 'reports/**/*.xml'
			echo 'Testing...'
			}
		}
		stage ('Deploy') {
			steps {
			// sh 'make publish'
			echo 'Deploying...'
			}
		}
		stage ('Deploy PROD') {
			steps {
				timeout(time:1, unit:'DAYS'){
			        	input message: 'Are you sure ?'  	
					}
				imput 'employing...'
			}
		}
	}	
}
