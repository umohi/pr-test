@Library('sayHello')
@Library('bfEmailFromGHId@dev-209-map-gh-to-bf-ids') _

node {
  stage('build') {
    sayHello
    sayHello "oooooooooooooooo"
    echo bfEmailFromGHId.doIt(this)
  }
}
