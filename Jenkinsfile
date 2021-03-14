pipeline {
    agent any
	println 'node main'
    stages {
	    println 'start'
        stage('push Code from branch to dev') {
            steps {
		 println 'inside function'
                git branch: 'branch', credentialsId: 'srsave', url: 'https://github.com/srsave/TestMerge.git'
            }
	}
    }
}

