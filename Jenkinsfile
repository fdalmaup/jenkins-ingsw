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
          sh './gradlew test'
        }

      }
    }

    stage('Validate') {
      steps {
        withGradle() {
          sh './gradlew check'
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