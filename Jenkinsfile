pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                sh '''
                  rm -rf *
                  git clone https://github.com/priya027v/hello-world-war
                '''
            }
        }

        stage('Build') {
            steps {
                sh '''
                  cd hello-world-war
                  mvn clean package
                '''
            }
        }

        stage('Deploy to JFrog') {
            steps {
                sh '''
                  cd hello-world-war
                  mvn deploy
                '''
            }
        }
    }
}



// pipeline {
//     agent any
//     stages {
//         stage('checkout') {
//             steps {
//                 sh "rm -rf *"
//                 sh 'git clone https://github.com/priya027v/hello-world-war'
//             }
//         }
//            stage('Build') {
//             steps {
//                    sh '''
//                     ls
//                     pwd
//                     cd hello-world-war
//                     echo $PWd
//                     ls
//                     mvn clean package
//                     echo "build completed"
//                 '''
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 withCredentials([usernamePassword(
//             credentialsId: 'jfrog',
//             usernameVariable: 'JFROG_USER',
//             passwordVariable: 'JFROG_API_KEY'
//         )])
//                 sh '''
//                   cp hello-world-war/target/*.war /opt/tomcat/webapps/

//                   /opt/tomcat/bin/shutdown.sh || true
//                   sleep 5
//                   /opt/tomcat/bin/startup.sh
//                 '''
//             }
//         }
//     }
// }
