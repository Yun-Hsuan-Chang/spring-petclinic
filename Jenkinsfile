pipeline {
    agent {
        docker {
            image 'maven:3.6-jdk-11-slim' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn install -DskipTests -Dcheckstyle.skip' 
            }
        }
    }
}