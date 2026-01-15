pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                sh "rm -rf *"
                sh 'git clone https://github.com/priya027v/hello-world-war'
            }
        }
           stage('Build') {
            steps {
                   sh '''
                    ls
                    pwd
                    cd hello-world-war
                    echo $PWd
                    ls
                    mvn clean package
                    echo "build completed"
                '''
            }
        }
           stage('Deploy') {
            steps {
                  sh '''
                    echo "Deploying WAR to Tomcat"

                    # Copy WAR file to Tomcat webapps
                      cp hello-world-war/target/*.war /opt/tomcat/webapps/

                    # Restart Tomcat
                      /opt/tomcat/bin/shutdown.sh || true
                    sleep 5
                    /opt/tomcat/bin/startup.sh

                    echo "Deployment completed"
                '''
            }
        }
    }
}
