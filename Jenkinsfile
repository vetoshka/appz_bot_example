pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
           args '-v /root/.m:/root/.m'
        }
    }
    stages {
   
        stage('Build') { 
            
            steps {
                sh 'mvn package'
                sh 'mvn -X exec:java -Dexec.mainClass=kpi.acts.appz.bot.hellobot.HelloWorldBot -Dexec.args="1705172028:AAFowiU_cY6xpZqX1Ole3vUrIhU5dINYSaw Kotyara"'
            }
        }
    }
}
