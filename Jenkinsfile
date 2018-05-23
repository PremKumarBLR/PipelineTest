node {
  stage('helloworld') {   
   echo 'Hello World'
  }

  stage('readfiles') {
    file = new File("${Jenkins.instance.getJob('JobName').workspace}/environment1").text
  }
}
