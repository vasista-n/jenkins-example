pipeline {
	agent {  label 'ubuntu cloud instance' }
	stages {
		stage('---clean---'){
			tools {
				maven 'Maven3.8.1'
			}
			steps {
				
				sh "mvn clean"
			}
		}
		stage('---test---') {
			tools {
				maven 'Maven3.8.1'
			}
			steps {
				
				sh "mvn test"
			}
		}
		stage('---package---'){
			tools {
				maven 'Maven3.8.1'
			}
			steps {
				
				sh "mvn package"
			}
		}
	}
	post {
		always {
			echo 'job was built successfully'
		}
	}
}
