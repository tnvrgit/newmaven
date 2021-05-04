@Library('shared-lib') _

import com.tnvr.shared-lib.gitCheckout

pipeline {
	agent any
	stages {
		stage('Git Checkout') {
			steps{
				gitCheckout('https://github.com/tnvrgit/newmaven')
			}
		}
	}
