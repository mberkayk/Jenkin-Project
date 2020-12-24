pipeline {

	agent any

	stages {
		steps {
			sh 'packer build --force ./box-config.json'
		}
	}
	
}
