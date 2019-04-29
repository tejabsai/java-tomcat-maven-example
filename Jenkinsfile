node(){
    
    stage('cloning'){
        checkout([$class: 'GitSCM', branches: [[name: '*/SIT-12']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/java-tomcat-maven-example.git']]])
        echo "cloning"
    }
     stage('building'){
        sh label: '', script: '''ls
mvn package
cd ..
'''
        echo "building"
    }
     stage('Sonar Analysis'){
        echo "Sonar analysis"
    }
     stage('Create Docker Image'){
        echo "Docker Image"
    }
     stage('Verify Docker Image'){
        echo "cloning"
    }
     stage('Deploy to dev'){
        echo "Deploy to dev"
    }
}
