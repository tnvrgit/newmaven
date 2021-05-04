@Library('shared-lib') _

pipeline {
	agent any
	stages {
		stage('Git Checkout') {
			steps{
				gitCheckout('https://github.com/tnvrgit/newmaven');
			}
		}
		stage('Git Checkout 2') {
			steps{
				script{
				def chk = new gitCheckout();
				chk.checkOutFrom('https://github.com/tnvrgit/test');
				}
			}
		}
	}
}
