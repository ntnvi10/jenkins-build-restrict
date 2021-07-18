pipeline {
    agent any
    
    stages {
        
        stage ("pipeline scripted") {
            steps {
                script { 
                    def userIdCause = currentBuild.getBuildCauses('hudson.model.Cause$UserIdCause') 
                    if (userIdCause.size()) {
                        error('Aborting Build due to manual start - thats not permitted!')
                    }
                }
            }
        }
        stage ("One") {
            steps {
                echo "Hello World"
            }
        } 
    }
}
