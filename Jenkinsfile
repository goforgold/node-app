pipeline {
  agent {
    docker {
      image 'node:8.9.4'
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
