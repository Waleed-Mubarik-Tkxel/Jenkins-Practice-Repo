pipeline {
    agent { docker { image 'php:8.2.8-alpine3.18' } }
    stages {
        stage('build') {
            steps {
                sh 'php --version'
            }
        }

        stage('production') {
            steps {
                echo 'Hurrah we are on prodcution!'
            }
        }
    }
}
