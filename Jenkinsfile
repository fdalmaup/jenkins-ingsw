pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        withGradle() {
          sh '''./gradlew build
./gradlew bootRun'''
        }

      }
    }

  }
}