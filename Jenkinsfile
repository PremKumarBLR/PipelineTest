pipeline {
    agent any
    stages {
        stage("Select Host endpoint") {
            steps {
                script {
                    sh "curl $ARTIFACTORY_URL" > ${WORKSPACE}/list" //we can query Artifactory here

                    env.LIST = readFile (file: "/var/lib/jenkins/NonProd") //Read some file into a variable

                    env.RELEASE_SCOPE = input message: 'User input required', ok: 'Release!',
                            parameters: [choice(name: 'RELEASE_SCOPE', choices: env.LIST, description: 'What is the release scope?')] //Provides input list
                }
                echo "Release scope selected: ${env.RELEASE_SCOPE}"
            }
        }
    }
}
