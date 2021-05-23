pipeline {
   agent any
   environment {
       color = "blue"
   }
   stages{
      stage('Build') {
            steps {
                script {
                    def commit = checkout scm
                    // we set BRANCH_NAME to make when { branch } syntax work without multibranch job
                    env.BRANCH_NAME = commit.GIT_BRANCH.replace('origin/', '')

                    //actually build ...
                }
            }
        }
   }
}


