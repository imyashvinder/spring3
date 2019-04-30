ansiColor('xterm') {
node('master') {
        properties ([
            buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '10')),
            [$class: 'RebuildSettings', autoRebuild: false, rebuildDisabled: false],
            ])

         if("${BRANCH_NAME}" == "dev"){
            stage("mvn clean") {
	       checkout scm
               sh '''
               echo "${WORKSPACE}"
               cd "${WORKSPACE}"
               ls -l
               /usr/local/bin/mvn352 clean
               /usr/local/bin/mvn352 compile
               /usr/local/bin/mvn352 clean package
               '''
            }
            stage("mvn compile") {
	       checkout scm
               sh '''
               echo "${WORKSPACE}"
               cd "${WORKSPACE}"
               ls -l
               /usr/local/bin/mvn352 compile
               '''
            }
            stage("mvn package") {
	       checkout scm
               sh '''
               echo "${WORKSPACE}"
               cd "${WORKSPACE}"
               ls -l
               /usr/local/bin/mvn352 clean package
               '''
            }
         }
         else if ("${BRANCH_NAME}" == "master") {
            stage("Build from master") {
               echo "This is master branch"
            }
         }
         else {
            stage("figure out branch") {
               echo "This is ....." + "${BRANCH_NAME}"
            }
         } 
         


        
      //   stage("Build from dev") {
      //      echo "This is dev branch"
      //   } 

      //   stage("Build from master") {
      //      echo "This is master branch"
      //   }
   
     //cleanWs(
     //       cleanWhenAborted: true,
     //       cleanWhenFailure: true,
     //       cleanWhenNotBuilt: true,
     //       cleanWhenSuccess: true,
     //       cleanWhenUnstable: true,
     //       deleteDirs: true
     //   )  
	
}
        
}



