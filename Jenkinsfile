//SCRIPTED

//DECLARATIVE
pipeline {
	agent any
	//agent { docker {image 'maven:3.9.1' } }
	//agent { docker {image 'node:19.9' } }
	environment {
	    dockerHome = tool 'myDocker'
	    mavenHome = tool 'myMaven'
	    PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Checkout'){
			steps {
			    sh 'mvn --version'
			    sh 'docker version'
				echo "Build"
				echo "PATH = $PATH"
				echo "BUILD_NUMBER = $env.BUILD_NUMBER"
				echo "BUILD_ID = $env.BUILD_ID"
				echo "JOB_NAME = $env.JOB_NAME"
				echo "BUILD_TAG = $env.BUILD_TAG"
				echo "BUILD_URL = $env.BUILD_URL"
			}
		}
		stage('Compile'){
		    steps {
		        sh "mvn clean compile"
		    }
		}
		stage('Test'){
            steps {
                sh "mvn test"
                }
            }
		stage('Integration test'){
            steps {
                sh "mvn failsafe:integration-test failsafe:verify"
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