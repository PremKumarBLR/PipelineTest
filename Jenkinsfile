node {
  stage('helloworld') {   
   echo 'Hello World'
  }

  stage('readfiles') {
    env.FILECONTENTS = readfile(file: 'environment1')
  }
}
