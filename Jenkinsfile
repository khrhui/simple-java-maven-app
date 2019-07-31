
    node {
        stage('Build') {
                def mvnHome = tool name: 'Maven-3', type: 'maven'
                sh "${mvnHome}/bin/mvn -B -DskipTests clean package"
        }
    }
