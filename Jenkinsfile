pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '/Users/rhui/Downloads/apache-maven-3.6.1/bin/mvn -B -DskipTests clean package'
            }
        }
    }
}
