pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Jenkins already checks out repo automatically
                echo 'SCM checkout done'
            }
        }

        stage('Build') {
            steps {
                sh '''
                pwd
                ls
                mvn clean package
                '''
            }
        }
    }
}
