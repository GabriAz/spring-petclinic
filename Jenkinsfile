pipeline {
  agent {
    docker {
      image 'openjdk:8-jre'
    }

  }
  stages {
    stage('java') {
      steps {
        sh 'echo $JAVA_HOME'
        sh './mvnw verify'
      }
    }
    stage('run') {
      steps {
        sh './mvnw spring-boot:run'
      }
    }
  }
}