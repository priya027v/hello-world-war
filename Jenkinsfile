pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                deleteDir()   // cleans workspace safely
                git 'https://github.com/priya027v/hello-world-war.git'
            }
        }

        stage('Build') {
            steps {
                dir('hello-world-war') {
                    sh 'mvn clean package'
                }
            }
        }
    }
}
