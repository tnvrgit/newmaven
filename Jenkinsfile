@Library('shared-lib') _


pipeline {
	agent any
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
}
