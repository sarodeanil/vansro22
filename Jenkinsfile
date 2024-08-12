pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                git branch: 'main', credentialsId: 'GithubLogin', url: 'https://github.com/sarodeanil/vansro22.git'
            }
        }
        stage('buid') {
            steps {
              sh "mvn clean pacage"
            }
        }
        
    }
}
