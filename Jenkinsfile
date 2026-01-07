pipeline {
agent any
parameters {
        string(name: 'CMD', defaultValue: 'cd', description: 'Command used to run or to build application')
        booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
        choice(name: 'CMD1', choices: ['Clean', 'validate', 'compile'], description: 'test package deploy')
       }
      stage {
      parallel {
         }
        stage('checkout') {
	    steps {

    withCredentials([
                        usernamePassword(
                        credentialsId: 'c7bd912f-283a-42e1-87eb-9af2c4260087',
                        usernameVariable: 'USERNAME',
                        passwordVariable: 'PASSWORD'
                    )
                ])
    {
 	    sh 'echo welcom'
	    sh 'echo $CMD $RUN_TESTS $$CMD1'
	    sh 'echo $USERNAME $PASSWORD'
	    }
	 }
    }
   }
  }

// pipeline {
//     agent any
//     parameters {
//         string(name: 'CMD', defaultValue: 'cd', description: 'Command used to run or build application')
//         booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run tests?')
//         choice(name: 'CMD1', choices: ['Clean', 'validate', 'compile', 'package','deploy', 'test'], description: 'test package deploy')
//     }

//     stages {
//         stage('Checkout') {
//             steps {
//                 sh '''
//                     echo "welcome"
//                     echo "$CMD $RUN_TESTS $CMD1"
//                 '''
//             }
//         }
//     }
// }
