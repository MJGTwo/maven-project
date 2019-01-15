pipeline {
  agent any

  tools {
    maven 'localMaven'
    jdk 'localJDK'
    docker 'docker'
  }

  stages {
    stage('Build'){
      steps {
        sh "mvn clean package"
        sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
      }
    }
  }
}
