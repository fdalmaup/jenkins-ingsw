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

  }
}