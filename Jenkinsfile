pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        withGradle() {
          sh '''java -version
pwd'''
        }

      }
    }

  }
}