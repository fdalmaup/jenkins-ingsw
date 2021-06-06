pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/fdalmaup/jenkins-ingsw', branch: 'main')
        sh '''gradle build
./gradlew bootRun'''
      }
    }

  }
}