pipeline {
    agent any
    tools {
        maven 'mvn_3.9.12'
    }
    stages {
        stage('build') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn clean test'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package -DskipTests'
            }
        }
    }
}
