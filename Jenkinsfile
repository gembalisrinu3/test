pipeline {
    agent {label 'windows'}
	tools { 
        git 'git' 
    }

    environment {
        VERSION = "${env.BUILD_TAG}"
    }

    options {
        disableConcurrentBuilds()
    }

    stages {
	    stage("Update Build's Display Name") {
            steps {
                script {
                    currentBuild.displayName = "#${env.BUILD_NUMBER} - ${params.stack}"
                }
            }
        }
		
		stage("SCM-dev") {
		    when {
                // Only run dev stage if a "dev" is requested
                	expression { params.stack == 'dev' }
            	}
            steps {
			checkout scm
            }
        }
	}
	}
