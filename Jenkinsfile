pipeline {

	agent any

	stages {
		stage ('build packer'){
			steps {
				sh 'PACKER_LOG=1 packer build --force ./box-config.json'
			}
		}
	}
	
}
