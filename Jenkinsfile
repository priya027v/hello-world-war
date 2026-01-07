pipeline {

    agent { label 'slave1' }

    parameters {
        string(name: 'env', defaultValue: 'dev', description: 'Target Environment')
        booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
        choice(name: 'MVN_GOAL',choices: ['clean', 'validate', 'compile', 'verify', 'deploy'],description: 'Maven goals'
        )
    }
    stages {

        stage('Parallel stage') {
            parallel {
                stage('Stage 1') {
                    steps {
                        sh 'echo "Running Stage 1"'
                    }
                }
                stage('Stage 2') {
                    steps {
                        sh 'echo "Running Stage 2"'
                    }
                }
            }
        }
        stage('credentials') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'priya_ID',
                        usernameVariable: 'priyadarshini',
                        passwordVariable: 'Password'),
                    usernamePassword(
                        credentialsId: 'tomcat_id',
                        usernameVariable: 'tomcat',
                        passwordVariable: 'PASSWORD')
                ]) {
                    sh 'echo $priyadarshini $Password'
                    sh 'echo $tomcat $PASSWORD'
                }
            }
        }
    }
}



// pipeline {
//     agent { label 'slave1' }

//     parameters {
//         string(name: 'env', defaultValue: 'dev', description: 'Target Environment')
//         booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run tests?')
//         choice(
//             name: 'MVN',
//             choices: ['clean', 'validate', 'compile', 'verify', 'deploy'],
//             description: 'Maven goals'
//         )
//     }
//     stages {
//         stage('Parallel stage') {
//             parallel {

//                 stage('Checkout step1') {
//                     steps {
//                         withCredentials([
//                             usernamePassword(
//                                 credentialsId: 'c7bd912f-283a-42e1-87eb-9af2c4260087',
//                                 usernameVariable: 'GIT_USER',
//                                 passwordVariable: 'GIT_PWD')
//                         ]) {
//                             sh '''
//                                 echo "Checkout completed step1"
//                                 echo "Using credential 1"
//                                 echo "User: $GIT_USER"
//                             '''
//                         }
//                     }
//                 }
//                 stage('Environment Info step2') {
//                     steps {
//                         withCredentials([
//                             usernamePassword(
//                                 credentialsId: 'priya_ID',
//                                 usernameVariable: 'JENKINS_USER',
//                                 passwordVariable: 'JENKINS_PWD')
//                         ]) {
//                             sh '''
//                                 echo "Environment completed step2"
//                                 echo "Using credential 2"
//                                 echo "User: $JENKINS_USER"
//                             '''
//                         }
//                     }
//                 }
//             }
//         }
//     }
// }

// pipeline {
//     agent { label 'slave1' }
//     parameters {
//         string(name: 'env', defaultValue: 'dev', description: 'Target Environment')
//         booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
//         choice(name: 'MVN',choices: ['clean', 'validate', 'compile', 'verify', 'deploy'],description: 'Maven goals')
//     }
//     stages {
//         stage('Parallel stage') {
//             parallel {
//                 stage('Checkout step1') {
//                     steps {
//                     sh 'echo "Checkout completed step1"'
//                     }
//                 }
//                 stage('Environment Info step2') {
//                     steps {
// 							sh 'echo "Environment completed step2 "'
//                     }
//                 }
//             }
//         }
//     }
// }





































// pipeline {
//     agent any

//     parameters {
//         string(name: 'CMD', defaultValue: 'cd', description: 'Command used to run or build application')
//         booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
//         choice(name: 'CMD1', choices: ['Clean', 'validate', 'compile'], description: 'test package deploy')
//     }

//     stages {
//         stage('Checkout') {
//             steps {
//                 withCredentials([
//                     usernamePassword(
//                         credentialsId: 'c7bd912f-283a-42e1-87eb-9af2c4260087',
//                         usernameVariable: 'USERNAME',
//                         passwordVariable: 'PASSWORD'
//                     )
//                 ]) 
//     {
//  	sh 'echo welcom'
// 	    sh 'echo $CMD $RUN_TESTS $$CMD1'
// 	    sh 'echo $USERNAME $PASSWORD'
// 	    }
// 	 }
//     }
//    }
//   }

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
