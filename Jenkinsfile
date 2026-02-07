pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building project'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to production'
            }
        }
    }

    post {
        always {
            echo 'POST BLOCK EXECUTED'
            emailext(
                to: 'tejaskalal1125@gmail.com',
                subject: 'PIPELINE EXECUTED SUCCESSFULLY',
                body: 'If you receive this email, pipeline notifications are working.'
            )
        }
    }
}
