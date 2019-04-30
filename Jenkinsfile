ansiColor('xterm') {
node('master') {
        properties ([
            buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '10')),
            [$class: 'RebuildSettings', autoRebuild: false, rebuildDisabled: false],
            ])
      
         println "${BRANCH_NAME}"

      //   stage("dev branch") {
      //      echo "this is dev branch"
      //   } 

      //   stage("master branch") {
      //      echo "this is master branch"
      //   }
   
     cleanWs(
            cleanWhenAborted: true,
            cleanWhenFailure: true,
            cleanWhenNotBuilt: true,
            cleanWhenSuccess: true,
            cleanWhenUnstable: true,
            deleteDirs: true
        )  
	
}
        
}



