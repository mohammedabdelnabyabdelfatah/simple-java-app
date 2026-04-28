node{
    git branch: 'main', url: 'https://github.com/mohammedabdelnabyabdelfatah/simple-java-app.git'
    stage('build'){
        try{
            sh'echo "build stage"'
        }
        catch(Exception e){
            sh'echo "exception found"'
            throw e
        }
    }  // This closing brace was missing for the stage('build') block
    
    stage('test'){
        if(env.BRANCH_NAME == "feat"){
            sh 'echo "test stage"'
        }
        else{
            sh'echo "skip test stage"'
        }
    }  // This closing brace was missing for the stage('test') block
}  // This closing brace closes the node block