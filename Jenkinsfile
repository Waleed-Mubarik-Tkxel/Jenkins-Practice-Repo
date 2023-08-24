pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'php --version'
            }
        }

        stage('production') {
            steps {
                echo "Hurrah we are on prodcution!"
            }
        }
    }
}
