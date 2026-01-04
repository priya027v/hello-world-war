pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                sh "rm -rf *"
                sh "git clone https://github.com/priya027v/hello-world-war"
            }
        }
          stage('Build') {
            steps {
                mvn clean package
            }
        }
    }
}

