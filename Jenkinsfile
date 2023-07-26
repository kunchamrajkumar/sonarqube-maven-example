node {

  stage ('checkout'){
           git branch: 'master', credentialsId: 'git_creds', url: 'https://github.com/kunchamrajkumar/tomcat-root-war.git'
 
         }

   stage ('build'){ 
        withMaven(globalMavenSettingsConfig: '', jdk: 'java', maven: 'maven', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn clean package'
           }
   
   }
