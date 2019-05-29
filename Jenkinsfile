@Library('sayHello') _

pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
		sayHello
		sayHello "oooooooooooooooo"
                sh 'env'
            }
        }
    }
}

