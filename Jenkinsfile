pipeline {
    agent any
environment{
    PATH="${PATH}:/opt/maven/bin"
}
    stages {
        stage('clone project from github') {
            steps {
                git branch: 'main', url: 'https://github.com/sarodeanil/vansro22.git'
            }
        }
        stage('buid the code') {
            steps {
            sh 'mvn clean package'
            }
        }
