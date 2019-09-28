node(){
triggers {
         cron('* * * * *')
         
    }
    stage('Clone'){
       checkout([$class: 'GitSCM', branches: [[name: '*/SIT-33']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/java-tomcat-maven-example.git']]]) 
    }
    stage('build'){
      sh label: '', script: 'mvn package'
    }
}
