pipeline {
    agent {
        docker {
            image 'maven:3.8.1-openjdk-11'
           args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
   
        stage('Build') { 
            
            steps {
                sh 'mvn -e compile exec:java'
                sh 'mvn clean install'
                sh 'mvn  exec:java -Dexec.mainClass=kpi.acts.appz.bot.hellobot.HelloWorldBot -Dexec.args="1650435543:AAEbfZYv-rwcbYQqa3ZUPpOv-mr1NHNJ_pw frog"'
            }
        }
    }
}
