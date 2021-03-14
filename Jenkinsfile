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
                git.exe add -A
                git.exe reset --hard HEAD
                git.exe merge 'TestMerge/branch'
                git.exe commit -m "Merged develop branch to master"
                git.exe push TestMerge branch
            }
   	 }
    }
}
