pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                def mvnHome = tool name: 'Maven-3', type: 'maven'
                sh '${mvnHome}/bin/mvn -B -DskipTests clean package'
            }
        }
    }
}
