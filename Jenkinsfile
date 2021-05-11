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
                git url: "https://github.com/KotyaraSingleCat/appz_bot_example.git"
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn clean install'
                sh' mvn -X exec:java -Dexec.mainClass=kpi.acts.appz.bot.hellobot.HelloWorldBot "-Dexec.args="1705172028:AAFowiU_cY6xpZqX1Ole3vUrIhU5dINYSaw" "Kotyara""'
            }
        }
    }
}
