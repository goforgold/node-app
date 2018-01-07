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
        sh 'packer build -var \'aws_access_key=AKIAIXXNI7MARFYU4CKA\' -var \'aws_secret_key=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\' packer/packer.json'
      }
    }
  }
  environment {
    npm_config_cache = 'npm-cache'
  }
}