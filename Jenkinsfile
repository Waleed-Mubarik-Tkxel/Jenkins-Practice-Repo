pipeline {
    agent { docker { image 'php:8.2.8-alpine3.18' } }
    parameters {
        booleanParam (name 'isAllowed', defaultValue: true, description: 'conditional is allowed')
        choice(name 'BuildVersion': ['2.0.0', '2.1.0'], description: 'versions')
    }
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
