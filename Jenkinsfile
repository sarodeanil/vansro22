pipeline {
    agent any
    environment{
        PATH="${PATH}:/opt/maven/bin"

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
    }
}
