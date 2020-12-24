pipeline {

	agent any

	stages {
		stage ('build packer'){
			steps {
				sh 'packer build -v --force ./box-config.json'
			}
		}
	}
	
}
