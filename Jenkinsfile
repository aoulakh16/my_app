pipeline {
    agent any 
    tools {
        maven 'maven 3.6.2'
    }
    stages {
        stage('Copy Repo and clean') { 
            steps {
                 sh "mvn clean"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package"
            }
        }
    }
}
