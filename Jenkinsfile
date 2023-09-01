pipeline {
    agent { docker { image 'php:8.2.8-alpine3.18' } }
    parameters {
        string (name: "user", defaultValue: "Waleed Mubarik", description: "Admin user name")
        booleanParam (name: 'isAllowed', defaultValue: true, description: 'conditional is allowed')
        choice(name: 'BuildVersion', choices: ['2.0.0', '2.1.0'], description: 'versions')
    }
    stages {
        stage('build') {
            when {
                expression {
                    params.isAllowed
                }
            }
            steps {
                sh 'php --version'
            }
        }

        stage('development') {
            steps {
                echo "development in progress by ${params.user}"
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
