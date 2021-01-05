pipeline {

	agent any

	stages {
		stage ('build packer'){
			steps {
				sh 'PACKER_LOG=1 packer build --force ./box-config.json'
			}
		}
	}
	post {
		success{
			s3Upload consoleLogLevel: 'INFO', dontSetBuildResultOnFailure: false, dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'mberkayk.jenkins-bucket', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: false, selectedRegion: 'us-west-2', showDirectlyInBrowser: false, sourceFile: 'deneme.txt', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 'aws-profile', userMetadata: []
		}
	}	
}
