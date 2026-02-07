pipeline {

  agent any

  stages {

    stage('Build') {
      steps {
        echo "Building application"
      }
    }

    stage('Deploy') {
      steps {
        sh 'echo Deploying application'
      }
    }
  }

  post {

    success {
      emailext(
        to: 'tejaskalal2002@gmail.com',
        subject: 'Jenkins Build SUCCESS',
        body: 'Build and deployment completed successfully.',
        mimeType: 'text/plain'
      )
    }

    failure {
      emailext(
        to: 'tejaskalal2002@gmail.com',
        subject: 'Jenkins Build FAILED',
        body: 'Build or deployment failed. Please check Jenkins console.',
        mimeType: 'text/plain'
      )
    }
  }
}
