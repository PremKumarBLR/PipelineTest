node {
pipeline {
    agent any
    stages {
        stage("Select Host endpoint") {
            steps {
                script {
                   file = new File("/var/lib/jenkins/NonProd").text
                }
                echo "$file"
            }
        }
    }
}
