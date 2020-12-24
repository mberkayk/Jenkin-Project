pipeline {

	agent any

	stages {
		stage ('build packer'){
			steps {
				sh 'packer build --force ./box-config.json'
			}
		}
	}
	
}
