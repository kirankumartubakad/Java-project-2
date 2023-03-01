pipeline {
    agent any 
    environment {
        PATH = "/usr/bin/mvn:$PATH"{    
        }
        stage("build code"){
            steps{
                sh "mvn clean install"        
            }
        }    
        stage("deploy"){
            steps{
                sshagent(['36ee9ae4-be9d-438f-9db7-ae70e3035833']) {
    scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/java1/target/onlinebookstore.war ubuntu@3.108.254.7:/opt/tomcat/apache-tomcat-9.0.68/webapps
}
            }
        }
    }
}
