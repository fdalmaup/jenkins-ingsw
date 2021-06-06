pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        withGradle() {
          sh './gradlew build'
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
        sh './gradlew bootRun --args=\'--server.port=8888\''
      }
    }

  }
}