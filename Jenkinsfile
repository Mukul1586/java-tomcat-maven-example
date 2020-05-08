node{
     def mvnHome = tool name: 'maven-3', type: 'maven' 
     
     environment{
     NAME=' Mukul'
     LASTNAME = 'Sharma'
     }
      stage('Checkout'){
         git 'https://github.com/LovesCloud/java-tomcat-maven-example'
       
      }  
      stage('Build'){
         //// Get maven home path and build
        sh "${mvnHome}/bin/mvn clean package -Dmaven.test.skip=true"
      }
   //  stage ('Test-JUnit'){
     //    sh "'${mvnHome}/bin/mvn' test surefire-report:report"
   //   }  
    
      stage('Deploy') {   
           
       sh "'echo ${NAME} ${LASTNAME}'"
          
   //         sshagent(['Tomcat-jenkins']) {
   //            sh 'scp -o StrictHostKeyChecking=no target/tomcatdeploymnetdemo.war jenkins@35.193.54.220:/opt/tomcat/webapps'
              
        
         
     }
      
 }
