//@Library('sayHello')
@Library('bfEmailFromGHId') 
import com.barefootnetworks.jenkins.sharedlibrary.BFEmailFromGH

def emailUtil = new bfEmailFromGHId(this)

node {
  stage('build') {
  	sh 'env'
    // sayHello
    // sayHello "oooooooooooooooo"
    emailUtil.emailAuthor()
  }
}
