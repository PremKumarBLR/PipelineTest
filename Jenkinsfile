node {
  stage('helloworld') {   
   echo 'Hello World'
  }

  stage('readfiles') {
    checkout scm
    def filecontents = readFile (file: 'environment1')
    //def files = findFiles(glob: '*.*') echo """${files[0].name} ${files[0].path} ${files[0].directory} ${files[0].length} ${files[0].lastModified}"""
    env.STACK = readFile (file: "environment1") //Read some file into a variable
    env.ENVIRONMENT = input message: 'User input required', ok: 'Release to Environment!',
                        parameters: [choice(name: 'ENVIRONMENT', choices: env.STACK, description: 'What is the ENVIRONMENT?')] //Provides input list
  }
}
