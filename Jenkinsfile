//dsafkick ass moreffasfddddddddddd
pipeline {
    agent { label 'ubuntu18slave' }
    stages {
        stage('build') {
            steps {
                  sh 'java -version'
            }
        }
	stage('last') {
	    steps {
              sh "echo almost"
	    	  sh "echo done"
	      githubNotify account: 'damnednforsaken', context: 'Final Test', credentialsId: 'y', description: 'This is an example', repo: 'testjenkins', sha: "${GIT_COMMIT}", status: 'SUCCESS', targetUrl: 'https://40.76.25.25'
      //githubNotify description: 'This is a shorted example',  status: 'SUCCESS'
	    }
	}
    }
}
