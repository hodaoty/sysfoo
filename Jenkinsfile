pipeline {
  agent any
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
        archiveArtifacts '**/target/*.war '
        sh 'echo "Done"'
      }
    }

  }
  tools {
    maven 'mvn_3.9.12'
  }
}