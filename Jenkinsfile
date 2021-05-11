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
                sh 'mvn clean package'
                sh "mvn -X exec:java -Dexec.mainClass=kpi.acts.appz.bot.hellobot.HelloWorldBot -Dexec.args="'1650435543:AAEbfZYv-rwcbYQqa3ZUPpOv-mr1NHNJ_pw' 'frog'""
            }
        }
    }
}
