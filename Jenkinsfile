ansiColor('xterm') {
node('master') {
        properties ([
            buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '10')),
            [$class: 'RebuildSettings', autoRebuild: false, rebuildDisabled: false],
            ])
      
         println "${BRANCH_NAME}"


         if("${BRANCH_NAME}" == "dev"){
            stage("Build from dev") {
               echo "This is dev branch"
            }
         }
         else if ("${BRANCH_NAME}" == "master") {
            stage("Build from master") {
               echo "This is master branch"
            }
         }
         else {
            stage(figure out branch) {
               echo "This is ....." + "${BRANCH_NAME}"
            }
         } 
         


        
      //   stage("Build from dev") {
      //      echo "This is dev branch"
      //   } 

      //   stage("Build from master") {
      //      echo "This is master branch"
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



