node {
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
            
        
   }
}
