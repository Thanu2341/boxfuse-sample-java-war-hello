pipeline {
    agent { label 'slave1' }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Thanu2341/boxfuse-sample-java-war-hello.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Archive WAR') {
            steps {
                archiveArtifacts artifacts: 'target/*.war', fingerprint: true
            }
        }
    }
}
