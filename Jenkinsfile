node {

  stage ('checkout'){
           git branch: 'master', credentialsId: 'git_creds', url: 'https://github.com/kunchamrajkumar/tomcat-root-war.git'
 
         }

   stage ('build'){ 
        withMaven(globalMavenSettingsConfig: '', jdk: 'java', maven: 'maven', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn clean package'
           }
   }
  stage('sonar.scan'){


   
      sh " mvn sonar:sonar \
  -Dsonar.host.url=http://54.163.127.180:9000 \
  -Dsonar.login=3f3c359d7550689ccbe32c57df94a1ab16397d63 " 
  

  }
     
   }
