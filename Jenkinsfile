@Library('shared-lib') _


pipeline {
	agent any
	tools { 
        	maven 'Maven3.6.3' 
        	jdk 'jdk1.8' 
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
	}
	post { 
        	always { 
            		cleanWs()
        	}
    	}
}
