pipeline {
    agent any 
    tools {
        maven 'maven 3.6.2'
    }
    stages {
        stage('Copy Repo and clean') { 
            steps {
                 sh "mvn clean -f my_app"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f my_app"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f my_app"
            }
        }
    }
}
