pipeline {
    agent any
    
    tools {
        maven 'maven3'
    }

    stages {
        stage('Git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/njamutoh/FullStack-Blogging-App.git'
            }
        }
        
        stage('Compile') {
            steps {
                sh "mvn compile"
            }
        }
        
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        
        stage('Package') {
            steps {
                sh "mvn package"
            }
        }
    }
}
