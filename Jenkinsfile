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
		    println 'insideupdate'
                git add: '-A'
                git reset: '--hard HEAD'
                git merge: 'TestMerge/branch'
                git commit: '-m "Merged develop branch to master"'
                git push: 'TestMerge branch'
            }
   	 }
    }
}
