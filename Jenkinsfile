node (master) {
    ws("workspace/${env.JOB_NAME}") {  
        stage('helloworld') {
            echo 'Hello World'
        }

        stage('readfiles') {
            def ws = pwd()
            def context  = ws + "/testArtifact"
            def file = ws + '/file'
            sh 'touch ' + file
            sh 'ls ' + ws        
        }
    }
}
