@Library('my_library@main') _  // Correct syntax

pipeline {
    agent { label 'slave' }


    stages {
        stage('Checkout Code') {
            steps {
                checkoutCode()
            }
        }
    }
}
