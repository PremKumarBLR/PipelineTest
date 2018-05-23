node {
  stage('helloworld') {   
   echo 'Hello World'
  }

  stage('readfiles') {
    checkout scm
    def filecontents = readFile (file: 'environment1')
    // Select Environment
    env.STACK = readFile (file: "environment1") //Read some file into a variable
    env.ENVIRONMENT = input message: 'User input required', ok: 'Select Environment!',
                        parameters: [choice(name: 'ENVIRONMENT', choices: env.STACK, description: 'What is the ENVIRONMENT?')] //Provides input list
    env.LIST = readFile (file: "${env.ENVIRONMENT}") //Read some file into a variable
    // Release to Environment
    env.RELEASE_SCOPE = input message: 'User input required', ok: 'Release!',
                        parameters: [choice(name: 'RELEASE_SCOPE', choices: env.LIST, description: 'What is the release scope?')] //Provides input list
    echo "Release scope selected: ${env.RELEASE_SCOPE}"
    echo "Branch selected: ${env.BRANCH_NAME}"
  }
}
