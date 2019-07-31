pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                def mvnHome = tool name: '', type: 'maven'
                sh '${mvnHome}/bin/mvn -B -DskipTests clean package'
            }
        }
    }
}
