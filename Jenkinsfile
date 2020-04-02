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
		stage("SCM-dev") {
		 steps {
                script {
		    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'git', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/gembalisrinu3/test.git']]])
						}
				}
		}
	}
	}
