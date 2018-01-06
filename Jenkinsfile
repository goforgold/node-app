pipeline {
  agent {
    docker {
      image 'build-container'
    }
  }
  environment {
      npm_config_cache = 'npm-cache'
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
  }
}
