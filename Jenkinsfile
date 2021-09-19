pipeline {
    environment {
        image_name = "kubedoom"
        DOCKER_HOST = "dindworker"
        PATH = "$PATH:${WORKSPACE}/bin/docker/"
    }

  agent any

  stages {
    stage('Building image') {
      steps{
        script {
          docker.build image_name + ":$BUILD_NUMBER"
        }
      }
    }
  }
}