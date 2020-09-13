pipeline{
    agent any
   
    stages{
        stage('calling function'){
            steps{
                  echo ">> Run deploy applications "
            }
       }
   }
    
    post { 
        always { 
            echo 'I will always say Hello!'
        }
        aborted {
            echo 'I was aborted'
        }
    }
}
