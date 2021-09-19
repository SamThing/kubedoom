pipeline {
    environment {
        image_name = "kubedoom"
    }

  agent any

  stages {
    stage('Building image') {
      steps{
        script {
          docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }
  }
}