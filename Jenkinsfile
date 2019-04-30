ansiColor('xterm') {
node('master') {
        properties ([
            disableConcurrentBuilds(),
            ])
        
        //checkout scm
        // stage('Checkout Bfa-Batch') {
        
        //     git branch: 'master',
        //         //credentialsId: 'git',
        //         //url: 'ssh://git@bitbucket.org/ntuclink/bfa-batch.git'
        //          url: 'ssh://git@github.com/imyashvinder/spring3.git'
        // }

        stage("Clone the Repo for Performing CI/CD") {
            git credentialsId: "3812f751-0658-484e-b8ba-1ef633fd0d4a", url: "ssh://git@github.com/imyashvinder/spring3.git"
        }

        
      //   stage("checkout scm")
      //   {
      //     checkout scm
      //   }
        
        stage("ls -l")
        {
         //   sh "cd bfaService"
           sh "ls -l"
        }

        stage("cd ")
        {
         //   sh "cd bfaService"
           sh "cd src; ls -l"
        }

        stage("cd ")
        {
         //   sh "cd bfaService"
           sh "cd src"
        }
        

        stage("cd ")
        {
         //   sh "cd bfaService"
           sh "ls -l"
        }
      //   stage("ls -l inside bfaService")
      //   {
      //      sh "ls -l bfaService"    
      //   }
        
      //   stage("ls -l inside bfaService")
      //   {
      //      sh "ls -l bfaService"
      //   }
	
}
        
}



