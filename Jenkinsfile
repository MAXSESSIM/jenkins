pipeline {
	agent any
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
		        sh 'node -v'
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
	}
}	
