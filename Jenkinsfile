@Library('shared-lib') _


pipeline {
	agent any
	tools { 
        	maven 'Maven3.6.3' 
        	jdk 'jdk9' 
    	}	
	stages {
		stage('Git Checkout') {
			steps{
				script{
				def chk = new com.tnvr.gitCheckout();
				chk.checkOutFrom('https://github.com/tnvrgit/test');
				}
			}
		}
		stage('Check Pre requisites') {
			withMaven{
				script{
					echo ${mvn -v}
					echo ${java -v}
				}
			}
		}
	}
	post { 
        	always { 
            		cleanWs()
        	}
    	}
}
