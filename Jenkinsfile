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
		stage('Run Maven') {
			steps{
				script{
					maven('clean package');
				}
			}
		}
		stage('Run Sonar') {
			steps{
				sh 'mvn sonar:sonar -Dsonar.projectKey=Demo-project -Dsonar.host.url=http://192.168.40.128:9001 -Dsonar.login=15e8fbeab0615b42bc7155ab446639aaeabe87fe
			}
		}
	}
	post { 
        	always { 
            		cleanWs()
        	}
    	}
}
