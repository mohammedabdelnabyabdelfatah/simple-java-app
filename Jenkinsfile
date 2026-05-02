pipeline{
    agent any
    stages{
        stage('build'){
            steps{
                script{
                    echo "build in progress"
                }
            }
        }
        stage('test'){
            steps{
                script{
                    echo "test in progress"
                }
            }
        }
    }
    post {
       success{ 
      slackSend channel: '#jenkins-ci', message: '"Build success - ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)" ', teamDomain: 'myproject-0ne3130', tokenCredentialId: 'slack-notification'
  }
    }
}

    
}