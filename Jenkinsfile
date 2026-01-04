pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                sh 'rm -rf *'
                sh 'git clone https://github.com/priya027v/hello-world-war'
            }
        }
        stage('build') {
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
