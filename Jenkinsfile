pipeline {

	agent any

	stages {
		stage ('build packer'){
			steps {
				s3Upload(profileName:"aws-profile",
								 entries: [
									bucket:jenkins-bucket ,
									sourceFile:deneme.txt],
									consoleLogLevel: "INFO",
									dontWaitForConcurrentBuildCompletion: false,
									dontSetBuildResultOnFailure: false,
									pluginFailureResultConstraint: "",
									userMetadata: [])
			}
		}
	}	
}
