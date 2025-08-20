@Library('my-shared-lib') _

pipeline {
    agent any

    options {
        skipDefaultCheckout()
    }

    stages {
        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Say Hello') {
            steps {
                sayHello('jenkins test') // from vars
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
