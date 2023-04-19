//SCRIPTED

//DECLARATIVE
pipeline {
	agent any
	//agent { docker {image 'maven:3.9.1' } }
	//agent { docker {image 'node:19.9' } }
	stages {
		stage('Build'){
			steps {
			    //sh 'mvn --version'
			    //sh 'node --version'
				echo "Build"
				echo "PATH = $PATH"
				echo "BUILD_NUMBER = $env.BUILD_NUMBER"
				echo "BUILD_ID = $env.BUILD_ID"
				echo "JOB_NAME = $env.JOB_NAME"
				echo "BUILD_TAG = $env.BUILD_TAG"
				echo "BUILD_URL = $env.BUILD_URL"
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
