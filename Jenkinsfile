pipeline {
    agent any
	
    stages {
	
        stage('push Code from branch to dev') {
            steps {
		 println 'inside function'
		    
               	     git branch: 'branch', credentialsId: 'srsave', url: 'https://github.com/srsave/TestMerge.git'
		     println 'Branch Success'
            }
	}
	stage('update master'){
            steps{
                sh 'git add -A'
                sh 'git reset --hard HEAD'
                sh 'git merge TestMerge/branch'
                sh 'git commit -m "Merged develop branch to master"'
                sh 'git push TestMerge branch'
            }
   	 }
    }
}
