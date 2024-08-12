pipeline {
    agent any
    environment{
        PATH="${PATH}:/opt/maven/bin"
    }

    stages {
        stage('clone') {
            steps {
                git branch: 'main', credentialsId: 'GithubLogin', url: 'https://github.com/sarodeanil/vansro22.git'
            }
        }
        stage('build') {
            steps {
                sh "mvn clean package"
            }
        }
         stage('deploy') {
            steps {
            sshagent(['tomcatlogin']) {
    sh "scp -o StrictHostKeyChecking=no target/vansro-1.0-SNAPSHOT.jar ec2-user@13.126.137.11:/opt/tomcat9/webapps"
}
            }
        }
    }
}
