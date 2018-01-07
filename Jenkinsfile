pipeline {
  agent {
    docker {
      image 'goforgold/build-container:latest'
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
