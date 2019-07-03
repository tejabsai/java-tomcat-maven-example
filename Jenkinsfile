node(){
    stage('cloning code'){
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/java-tomcat-maven-example.git']]])
    }
    stage('Building code'){
        sh label: '', script: 'mvn package'
        
    }
    stage('Nexus upload'){
        sh label: '', script: 'mvn deploy'
    }
    stage('Sonar analysis'){
        sh label: '', script: 'mvn sonar:sonar'
        
    }
    stage('create docker container'){
        
        
    }
    stage('Verify the container'){
        
    }
}
