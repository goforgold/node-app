pipeline {
  agent {
    docker {
      image 'goforgold/build-container:latest'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Create Packer AMI') {
      steps {
        sh '''sudo packer build -var \'aws_access_key=AKIAINVK627I4OKVC5PA\' -var \'aws_secret_key=sFZSEZ//pIOQQnSHf5yVYVWSVnB2naBEayVPMD
Tp\' packer/packer.json'''
      }
    }
  }
  environment {
    npm_config_cache = 'npm-cache'
  }
}