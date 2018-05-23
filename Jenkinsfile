node {
  stage('helloworld') {   
   echo 'Hello World'
  }

  stage('readfiles') {
    checkout scm
    def filecontents = readFile (file: 'environment1')
    //def files = findFiles(glob: '*.*') echo """${files[0].name} ${files[0].path} ${files[0].directory} ${files[0].length} ${files[0].lastModified}"""
    echo filecontents
  }
}
