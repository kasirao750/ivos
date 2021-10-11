pipeline {
	
	agent 'any'

	
	
	
	
	stages {
		
		stage('checkout') {
			steps {
				git branch: 'main', changelog: false, credentialsId: 'gitcred', poll: false, url: 'https://github.com/kasirao750/ivos.git'
			}
		}
		
		
		stage('compile') {
			steps {
				withAnt(installation: 'ant_1.10.11') {
					ant -f build.xml main
				}
			}
		}
		
		
		stage('print') {
			steps {
				echo "stage 3"
			}
		}
		
	
	
	}
}