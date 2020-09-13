
pipeline {
    agent none
    stages {
        stage('calling function'){
                  echo "Run deploy applications"
                  def publisher = LastChanges.getLastChangesPublisher "LAST_SUCCESSFUL_BUILD", "SIDE", "LINE", true, true, "", "", "", "", ""
                  publisher.publishLastChanges()
                  def changes = publisher.getLastChanges()
                  println(changes.getEscapedDiff())

                    for (commit in changes.getCommits()) {
                        println(commit)
                        def commitInfo = commit.getCommitInfo()
                        println(commitInfo)
                        println(commitInfo.getCommitMessage())
                        println(commit.getChanges())
                    }
                env.WORKSPACE = pwd()
                def version = readFile "${env.WORKSPACE}/doctest"
                echo version
           }
    }
    post { 
        always { 
            cleanWs()
        }
    }
}
