node(){
properties([[$class: 'JiraProjectProperty'], [$class: 'DatadogJobProperty', tagFile: '', tagProperties: ''], gitLabConnection('gitlab'), parameters([gitParameter(branch: '', branchFilter: '.*', defaultValue: 'master', description: 'select the branch for build', name: 'BRANCH_NAME', quickFilterEnabled: false, selectedValue: 'NONE', sortMode: 'NONE', tagFilter: '*', type: 'PT_BRANCH_TAG')])])
//checkout scm   
       
         stage('checkout'){
                checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: */"$BRACNH_NAME"]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/java-tomcat-maven-example.git']]]          
         }
stage('Maven Build') {         
         sh '''
                 mvn package
                
            '''
        }
stage('Docker Build') {         
         sh '''
         docker images
                // docker build -t testimage .
                 //docker run --name=newcontainer -d -p 9898:8080 testimage
            '''
        }
 }
