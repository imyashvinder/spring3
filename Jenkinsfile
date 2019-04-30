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
            git credentialsId: "git", url: "ssh://git@github.com/imyashvinder/spring3.git"
        }

        
        // stage("checkout scm")
        // {
        //   checkout scm
        // }
        
        stage("cd bfaService")
        {
           sh "cd bfaService"
           sh "ls -l"
        }
        
        stage("ls -l inside bfaService")
        {
           sh "ls -l bfaService"    
        }
        
        stage("ls -l inside bfaService")
        {
           sh "ls -l bfaService"
        }
	
}
        
}



