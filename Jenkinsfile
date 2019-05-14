def LINK_DOCKER_IMAGE = "maven:3.3.3"

pipeline {
  triggers {
    parameterizedCron(env.BRANCH_NAME == 'plugin-test' ? '''
# schedule every 4hours only on weekdays
*/2 * * * 1-5 % ABC=XYZ''' : '')
  }
    agent { docker { image "${env.GIT_BRANCH}" } }
    stages {
        stage('build') {
            steps {
                sh 'env'
            }
        }
    }
}
