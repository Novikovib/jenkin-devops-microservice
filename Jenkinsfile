//SCRIPTED

//DECLARATIVE
pipeline {
	//agent any
	//agent { docker {image 'maven:3.9.1' } }
	agent { docker {image 'node:13.9' } }
	stages {
		stage('Build'){
			steps {
			    //sh 'mvn --version'
			    sh 'node --version'
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
	}
	post{
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
