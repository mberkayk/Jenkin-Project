pipeline {

	agent any

	stages {
		stage ('build packer'){
			steps {
				sh 'PACKER_LOG=1 packer build --force ./box-config.json'
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
