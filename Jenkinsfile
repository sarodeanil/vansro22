pipeline {
    agent any
    environment{
        PATH="${PATH}:/opt/maven/bin"
    }
    stages {
        stage('clone') {
            steps {
                git branch: 'main', credentialsId: '8fd1fbac-0ddf-4f43-9ee3-12cf14479639', url: 'https://github.com/sarodeanil/vansro22.git'
            }
        }
        stage('buid') {
            steps {
              sh "mvn clean pacage"
            }
        }
        
    }
}
