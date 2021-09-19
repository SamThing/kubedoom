pipeline {
    environment {
        image_name = "kubedoom"
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