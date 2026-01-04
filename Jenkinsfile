pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh "rm -rf"
                git 'https://github.com/priya027v/hello-world-war.git'
            }
        }

        stage('Build') {
            steps {
                   sh '''
                   ls
                   pwd
                   cd hello-world-war
                   pwd
                   ls
                   mvn clean package
                '''
                }
            }
        }
    }
