//def LINK_DOCKER_IMAGE = "maven:3.3.3"
def LINK_DOCKER_IMAGE = env.GIT_BRANCH

println ("${env.GIT_BRANCH}")


pipeline {
  triggers {
    parameterizedCron(env.BRANCH_NAME == 'plugin-test' ? '''
# schedule every 4hours only on weekdays
*/2 * * * 1-5 % ABC=XYZ''' : '')
  }
    agent { docker { image "${LINK_DOCKER_IMAGE}" } }
    stages {
        stage('build') {
            steps {
                sh 'env'
            }
        }
    }
}
