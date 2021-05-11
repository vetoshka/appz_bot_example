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
                sh 'java -cp target/ kpi.acts.appz.bot.hellobot.HelloWorldBot "1650435543:AAEbfZYv-rwcbYQqa3ZUPpOv-mr1NHNJ_pw" "frog"'
            }
        }
    }
}
