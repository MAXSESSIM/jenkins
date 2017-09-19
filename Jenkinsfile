pipeline {
	agent {
		docker { image 'node:6.11.3.alpine' }
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
