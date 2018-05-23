node {
    ws("workspace/${env.JOB_NAME}") {  
        stage('helloworld') {
            echo 'Hello World'
        }
        
        stage('readfile') {
            echo 'Inside readfile Stage'
            env.WORKSPACE = pwd()
            def version = readFile "${env.WORKSPACE}/environment1"
            echo version
        }
    }
}
