pipeline {
    agent any

    parameters {
        string(name: 'CMD', defaultValue: 'cd', description: 'Command used to run or build application')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run tests?')
        choice(name: 'CMD1', choices: ['Clean', 'validate', 'compile', 'package','deploy', 'test'], description: 'test package deploy')
    }

    stages {
        stage('Checkout') {
            steps {
                sh '''
                    echo "welcome"
                    echo "$CMD $RUN_TESTS $CMD1"
                '''
            }
        }
    }
}
