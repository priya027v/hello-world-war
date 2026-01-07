pipeline {
    agent any

    parameters {
        string(name: 'CMD', defaultValue: 'cd', description: 'Command used to run or build application')
        booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
        choice(name: 'CMD1', choices: ['Clean', 'validate', 'compile'], description: 'test package deploy')
    }

    stages {
        stage('Checkout') {
            steps {
                sh '''
                    echo "welcome"
                    echo "CMD=${CMD}"
                    echo "RUN_TESTS=${RUN_TESTS}"
                    echo "CMD1=${CMD1}"
                '''
            }
        }
    }
}
