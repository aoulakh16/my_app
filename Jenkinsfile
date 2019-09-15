pipeline {
    agent any 
    tools {
        maven 'maven 3.6.2'
    }
    stages {
        stage('Copy Repo and clean') { 
            steps {
                 sh "mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f my-app"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}
