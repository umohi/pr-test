@Library('bf-jenkins-utils@develop')_

pipeline {
    agent any
	stages {
		stage ( 'dadf'){
			steps {
		    	script {
		    		stopPreviousRuns(this)	
		    	}
		    }
        }
        stage('build') {
        	steps {
          		sh 'env && exit 1'
          	}
        }   
    }
    

    post {
        always {
            script {
            	if (currentBuild.currentResult == 'FAILURE') { // Other values: SUCCESS, UNSTABLE
		            bfEmailFromGHId(this)
		        }
		        else {
		        	println "Build did not fail ${currentBuild.currentResult}: no email sent"
		        }
            }
        }
    }
}
