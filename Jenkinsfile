//dsafkick ass moreffasfddddddddddd
void setBuildStatus(String message, String state) {
  step([
      $class: "GitHubCommitStatusSetter",
      reposSource: [$class: "ManuallyEnteredRepositorySource", url: "https://github.com/DamnedNForsaken/testjenkins"],
      contextSource: [$class: "ManuallyEnteredCommitContextSource", context: "ci/jenkins/build-status"],
      errorHandlers: [[$class: "ChangingBuildStatusErrorHandler", result: "UNSTABLE"]],
      statusResultSource: [ $class: "ConditionalStatusResultSource", results: [[$class: "AnyBuildResult", message: message, state: state]] ]
  ]);
}


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
              sh "almost"
	    	  sh "echo done"
              setBuildStatus("Build succeeded", "SUCCESS");
	       //githubNotify description: 'This is a shorted example',  status: 'SUCCESS'
	    }
	}
    }
}

