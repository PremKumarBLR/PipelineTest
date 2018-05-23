node {
    ws("workspace/${env.JOB_NAME}") {  
        stage('helloworld') {
            echo 'Hello World'
        }

        stage('readfiles') {
            def ws = pwd()
            def envfile  = ws + "/environment1"
            env.STACK = readFile (file: "${envfile}") //Read some file into a variable
            echo ${env.STACK}
            env.ENVIRONMENT = input message: 'User input required', ok: 'Release!',
                                parameters: [choice(name: 'ENVIRONMENT', choices: env.STACK, description: 'What is the ENVIRONMENT?')] //Provides input list
            env.LIST = readFile (file: '${env.ENVIRONMENT}') //Read some file into a variable
            echo "File Contents : ${env.LIST}"

            env.RELEASE_SCOPE = input message: 'User input required', ok: 'Release!',
                                parameters: [choice(name: 'RELEASE_SCOPE', choices: env.LIST, description: 'What is the release scope?')] //Provides input list
            echo "Release scope selected: ${env.RELEASE_SCOPE}"
            echo "Branch selected: ${env.BRANCH_NAME}"
        }
    }
}
