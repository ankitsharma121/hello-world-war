pipeline {
    agent { label 'slave1' }
    stages {
        stage('clone step') {
            steps {
                sh 'rm -rf hello-world-war'
                sh 'git clone https://github.com/ankitsharma121/hello-world-war.git'
            }
        }
  stage('Build') {
            steps {
                sh 'mvn package'
            }
  }
      stage('Deploy step') {
            steps {
                sh 'sudo cp /home/slave1/workspace/deploy2/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.64/webapps/'      
            }
        }
    }
}
