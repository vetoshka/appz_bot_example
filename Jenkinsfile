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
                sh 'mvn clean install'
            }
        }
    }
}
