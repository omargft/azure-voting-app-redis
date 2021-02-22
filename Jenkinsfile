pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Build'){
         steps{
            sh(script: 'sudo docker images -a')
            sh(script: 'mkdir azure-vote ; cd azure-vote ; docker images -a ; sudo docker build -t jenkins-pipeline . ; docker images -a; cd ..')
         }
      }
   }
}
