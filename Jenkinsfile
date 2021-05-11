pipeline {
    agent {
        docker {
            image 'maven:3.8.1-openjdk-11'
           args '-v /var/jenkins_home/jobs/jj:/root/'
        }
    }
    stages {
   
        stage('Build') { 
            
            steps {
               
                sh 'mvn clean install'
                sh 'mvn -X exec:java -Dexec.mainClass="kpi.acts.appz.bot.hellobot.HelloWorldBot" -Dexec.args="1650435543:AAEbfZYv-rwcbYQqa3ZUPpOv-mr1NHNJ_pw frog"'
            }
        }
    }
}
