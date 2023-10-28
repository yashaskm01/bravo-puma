pipeline {
    agent any
    
    tools {
        maven 'maven'
    }

    stages {
        stage('git clone') {
            steps {
                git 'https://github.com/yashaskm01/bravo-puma.git'
            }
        }
        stage('validate') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
