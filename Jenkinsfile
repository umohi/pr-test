//@Library('sayHello')
@Library('bfEmailFromGHId') 
import com.barefootnetworks.jenkins.sharedlibrary
def emailUtil = new bfEmailFromGHId(this)

node {
  stage('build') {
  	sh 'env'
    // sayHello
    // sayHello "oooooooooooooooo"
    emailUtil.emailAuthor()
  }
}
