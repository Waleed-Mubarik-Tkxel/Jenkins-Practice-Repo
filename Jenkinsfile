pipeline {
    agent { docker { image 'php:8.2.8-alpine3.18' } }
    stages {
        stage('build') {
            when {
                expression {
                    BRANCH_NAME == 'DEV'
                }
            }
            steps {
                sh 'php --version'
            }
        }

        stage('development') {
            steps {
                echo 'development in progress '
                echo BRANCH_NAME
            }
        }

        stage('production') {
            steps {
                echo 'Hurrah we are on prodcution!'
            }
        }
    }
}
