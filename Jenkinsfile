pipeline {
    agent {label 'windows'}

   stages {
      stage('Hello') {
         steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'git', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/gembalisrinu3/test.git']]])
         }
      }
   }
}
