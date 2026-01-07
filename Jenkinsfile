pipeline {
agent any
parameters {
        string(name: 'CMD', defaultValue: 'cd', description: 'Command used to run or to build application')
        booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
        choice(name: 'CMD1', choices: ['Clean', 'validate', 'compile'], description: 'test package deploy')
    }

     stage {
       stage('checkout') {
	      steps {
         	sh 'echo welcom'
	        sh 'echo $CMD $RUN_TESTS $$CMD1'

	      }
      }
    }
  }
