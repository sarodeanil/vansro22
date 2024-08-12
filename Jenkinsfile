pipeline {
    agent any
    environment{
        PATH="$(PATH):/opt/maven/bin
    }
    stages {
        stage('clone') {
            steps {
                echo "clone from git"
            }
        }
        stage('buid') {
            steps {
              sh "mvn clean pacage"
            }
        }
        
    }
}
