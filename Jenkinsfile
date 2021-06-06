pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/fdalmaup/jenkins-ingsw', branch: 'main')
        sh '''echo $JAVA_HOME
./gradlew clean build
./gradlew bootRun'''
      }
    }

  }
}