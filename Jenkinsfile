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
}
