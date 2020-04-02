pipeline {
    agent {label 'windows'}
    tools {
        git 'git'
    }

   stages {
      stage('Hello') {
         steps {
            // git branch: 'master', gitTool: 'git', url: 'https://github.com/gembalisrinu3/test.git'
             checkout scm
            // checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'git', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/gembalisrinu3/test.git']]])
         }
      }
   }
}
