pipeline {
    /* specify nodes for executing */
    agent {
        label 'github-ci'
    }
 
    stages {
         stage('Do the deployment') {
            steps {
                echo ">> Run deploy applications "
            }
        }
    }
 
    /* Cleanup workspace */
    post {
       always {
           deleteDir()
       }
   }
}
