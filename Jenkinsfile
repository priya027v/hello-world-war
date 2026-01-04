pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf *'
               sh 'https://github.com/priya027v/hello-world-war'
            }
        }
        stage('Build') {
            steps {
                    sh '''
                    pwd
                    ls
                    cd hello-world-war
                    pwd
                    ls
                    mvn clean package
                '''
            }
        }
    }
}
