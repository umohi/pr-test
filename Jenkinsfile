//@Library('sayHello')
@Library('emailUtil') 
import com.barefootnetworks.jenkins.sharedlibrary.BFEmailFromGH

def emailUtil = new BFEmailFromGH(this)

node {
    try {
        stopPreviousRuns(this)
        stage('build') {
          
          	sh 'env'
            // sayHello
            // sayHello "oooooooooooooooo"
            //emailUtil.emailAuthor()
        }   
    }
    finally {
    	// Send an email only if the build fails
        if (currentBuild.currentResult == 'FAILURE') { // Other values: SUCCESS, UNSTABLE
            bfEmailFromGHId(this)
        }
        else {
        	println "Build did not fail: no email sent"
        }
    }
}
