pipeline {
    agent {
        docker {
            image 'maven:3.8.1-openjdk-11'
           args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('git') {
            steps {
                git "https://github.com/vetoshka/appz_bot_example.git"
            }
        }
        stage('Build') { 
            
            steps {
                sh 'mvn clean package'
                sh 'mvn -X exec:java -Dexec.mainClass=kpi.acts.appz.bot.hellobot.HelloWorldBot -Dexec.args=1650435543:AAEbfZYv-rwcbYQqa3ZUPpOv-mr1NHNJ_pw ,frog'
            }
        }
    }
}
