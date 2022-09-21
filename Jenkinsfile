pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                sh 'ssh root@172.31.7.160 "yum update -y"'
                sh 'ssh root@172.31.7.160 "amazon-linux-extras install java-openjdk11 -y"'
                sh 'ssh root@172.31.7.160 "wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.65/bin/apache-tomcat-9.0.65.tar.gz"'
                sh 'ssh root@172.31.7.160 "tar -xzvf  apache-tomcat-9.0.65.tar.gz"'
                sh 'ssh root@172.31.7.160 "rm -fr  apache-tomcat-9.0.65.tar.gz"'
                sh 'ssh root@172.31.7.160 "mv apache-tomcat-9.0.65 tomcat"'
                sh 'ssh root@172.31.7.160 "cd tomcat/bin &&sh startup.sh"'
            }
        }
       
    }
}