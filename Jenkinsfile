@Library('my-shared-lib') _

pipeline {
    agent any

    stages {
        stage('Say Hello') {
            steps {
                sayHello('Jenkins') // from vars
            }
        }

        stage('Use Utility Class') {
            steps {
                script {
                    def utils = new org.example.MyUtils(this)
                    utils.greet('Bob') // from src
                }
            }
        }
    }
}
