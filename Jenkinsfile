pipeline {
    agent any
    
    stages {
        stage('Build') {
            def mvnHome = tool name: 'maven-3', type: 'maven'
            steps {
                sh "${mvnHome}/bin/mvn -B -DskipTests clean package"
            }
        }
        stage('Test') {
            def mvnHome = tool name: 'maven-3', type: 'maven'
            steps {
                sh "${mvnHome}/bin/mvn test"
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
            }
        }
    }
}
