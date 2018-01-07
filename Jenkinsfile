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
          withCredentials([usernamePassword(credentialsId: 'ada90a34-30ef-47fb-8a7f-a97fe69ff93f', passwordVariable: 'AWS_SECRET', usernameVariable: 'AWS_KEY')]) {
            sh 'packer build -var \'aws_access_key=${AWS_KEY}\' -var \'aws_secret_key={$AWS_SECRET}\' packer/packer.json'
        }
      }
    }
  }
  environment {
    npm_config_cache = 'npm-cache'
  }
}
