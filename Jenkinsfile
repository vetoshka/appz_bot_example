pipeline {
    agent {
        docker {
            image 'maven:3.8.1-openjdk-11'
           args '-v /root/.m:/root/.m'
        }
    }
    stages {
   
        stage('Build') { 
            
            steps {
               
                sh 'mvn package'
               sh' mvn clean install org.codehaus.mojo:exec-maven-plugin:1.1.1:java -Dexec.mainClass="kpi.acts.appz.bot.hellobot.HelloWorldBot " -e'
            }
        }
    }
}
