node {

  stage ('checkout'){
           git branch: 'master', credentialsId: 'git_creds', url: 'https://github.com/kunchamrajkumar/sonarqube-maven-example.git'
 
         }

   stage ('build'){ 
        withMaven(globalMavenSettingsConfig: '', jdk: 'java', maven: 'maven', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn package'
           }
   }
  /* stage ('sonar scan') {   
     withMaven(globalMavenSettingsConfig: '', jdk: 'java', maven: 'maven', mavenSettingsConfig: '', traceability: true) {
            withSonarQubeEnv(credentialsId: 'sonar_newID') {
    sh " mvn sonar:sonar"
}
     }

  
  }*/

  
  /*stage('sonar.scan'){

withMaven(globalMavenSettingsConfig: '', jdk: 'java', maven: 'maven', mavenSettingsConfig: '', traceability: true) {
   
      sh " mvn sonar:sonar \
  -Dsonar.projectKey=tomcat_sample \
  -Dsonar.host.url=http://54.157.227.139:9000 \
  -Dsonar.login=56e5ad0a695eda6b8d8135b4488e048bb5bde3d4 " 
}

  }*/
     
   }
