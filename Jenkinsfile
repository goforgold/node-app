pipeline {
  agent {
    docker {
      image 'node'
      args '8.9.4'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
  }
}