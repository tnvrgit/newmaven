@Library('shared-lib') _

pipeline {
	agent any
	stages {
		stage('Git Checkout') {
			steps{
				gitCheckout('https://github.com/tnvrgit/newmaven')
			}
		}
	}
