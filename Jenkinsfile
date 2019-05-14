//def LINK_DOCKER_IMAGE = "maven:3.3.3"
def LINK_DOCKER_IMAGE = "${env.GIT_BRANCH}"

pipeline {
    environment {
        SSH_KEY = credentials('ssh-key')
	OOO = "${env.GIT_BRANCH}"
    }
  triggers {
    parameterizedCron(env.BRANCH_NAME == 'plugin-test' ? '''
# schedule every 4hours only on weekdays
*/2 * * * 1-5 % ABC=XYZ''' : '')
  }
    agent { docker { image "${OOO}" } }
    stages {
        stage('build') {
            steps {
                sh 'env'
            }
        }
    }
}
