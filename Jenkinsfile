pipeline{

  agent any

  stages{

    stage ('Build'){
      steps{
        echo "Building branch:${BRANCH_NAME}"
      }
    }

    stage ('Deploy'){
      when{
        branch 'master'
      }

      steps{
        echo "Deploying to production"
      }
    }
  }
  
  post{
    success{
      emailext(
        to:'tejaskalal2002@gmail.com',
        subject:"Successfully deployed - ${env.JOB_NAME} - ${env.BRANCH_NAME} to production",
        body:"The deployment of - ${env.BRANCH_NAME} to production was successful."
      )
    }
    failure{
      emailext(
        to:'tejaskalal2002@gmail.com',
        subject:"Deployment failed - ${env.JOB_NAME} - ${env.BRANCH_NAME} to production",
        body:"The deployment of - ${env.BRANCH_NAME} to production failed."
      )
    }
  }
}

