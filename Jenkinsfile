pipeline {
  triggers {
    parameterizedCron(env.BRANCH_NAME == 'plugin-test' ? '''
# schedule every 4hours only on weekdays
*/2 * * * 1-5 % ABC=XYZ''' : '')
  }
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'env'
            }
        }
    }
}
