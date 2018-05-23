node {
  stage('helloworld') {   
   echo 'Hello World'
  }

  stage('readfiles') {
    env.FILECONTENTS = readFile (file: 'environment1')
  }
}
