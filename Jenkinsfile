node{
     def mvnHome = tool name: 'maven-3', type: 'maven' 
     def first = 'Mukul'
     def last = 'Sharma'
     
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
           
     sh label: '', script: "echo \'${first} ${last}\'"
           println  " i am sexy and i know it"
          
   //         sshagent(['Tomcat-jenkins']) {
   //            sh 'scp -o StrictHostKeyChecking=no target/tomcatdeploymnetdemo.war jenkins@35.193.54.220:/opt/tomcat/webapps'
              
        
         
     }
      
 }
