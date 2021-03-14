pipeline {
    agent any
    stages {
        stage('push Code from branch to dev') {
            steps {
		 
                git branch: 'branch', credentialsId: 'srsave', url: 'https://github.com/srsave/TestMerge.git'
            }
	}
	
}
