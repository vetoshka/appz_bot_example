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
               
                sh 'mvn package docker:build'
                sh 'mvn -X exec:java -Dexec.mainClass="kpi.acts.appz.bot.hellobot.HelloWorldBot" -Dexec.args="1650435543:AAEbfZYv-rwcbYQqa3ZUPpOv-mr1NHNJ_pw frog"'
            }
        }
    }
}
