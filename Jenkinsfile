node(){
  stage("clone"){
   checkout([$class: 'GitSCM', branches: [[name: '*/dev-with-dockerfile']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'Default', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/java-tomcat-maven-example.git']]])
  }
  stage("Maven-Build"){
     bat 'mvn package'
  }
  stage("Sonar analyis"){
      echo "Sonar analysis"
  }
  stage("Creating and running the docker image"){
      echo "Write the steps for docker ss or bat"
      //sh '''
     // docker build -t testimage .
     // docker run -d -p 8888:8080
    //  '''
  }
  stage("Verification"){
      echo "how to verify"
  }
   
}
