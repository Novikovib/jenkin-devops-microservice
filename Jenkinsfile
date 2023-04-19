//SCRIPTED

//DECLARATIVE
pipeline {
	agent any
	stages {
		stage('Build'){
			steps {
				echo "Build"
			}
		}
		stage('Test'){
                        steps {
                                echo "Test"
                        }
                }
		stage('Integration test'){
                        steps {
                                echo "Integration Test"
                        }
                }
	} post{
		always {
			echo "I'm awesome. I run always"
		}
		success {
                        echo "I'm run when you are successful"
                }
		failure {
                        echo "I'm run when you are fail"
                }
	}
}
