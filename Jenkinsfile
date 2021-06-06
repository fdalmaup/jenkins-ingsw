pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        withGradle() {
          sh '''./gradlew build
./gradlew bootRun --args=\'--server.port=8888\''''
        }

      }
    }

    stage('Test') {
      steps {
        withGradle() {
          sh 'gradle test'
        }

      }
    }

    stage('Validate') {
      steps {
        withGradle() {
          sh 'gradle check'
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployando'
      }
    }

  }
}