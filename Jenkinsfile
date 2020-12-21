pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn compile'
        sh 'echo \'complete building\''
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
  tools {
    maven 'Maven 3.6.3'
  }
}