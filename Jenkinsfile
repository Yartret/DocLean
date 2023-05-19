pipeline {
    agent any
    stage('Checkout') {
    steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github-credentials', url: 'https://github.com/Yartret/DocLean.git']]])
         }
    } 
}
