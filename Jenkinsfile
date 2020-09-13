node {

def myfun = load 'testfun.groovy'
pipeline{
    agent any
    environment{
        REPO_PATH='/home/manish/Desktop'
        APP_NAME='test'
    }
    stages{
        stage('calling function'){
            steps{
                script{
                    myfun('${REPO_PATH}','${APP_NAME}')
                }
             }
         }
     }
  }

}
