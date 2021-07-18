pipeline {
    agent any
    
    stages {
        
        stage ("pipeline scripted") {
            steps {
                script { 
                    def userIdCause = currentBuild.getBuildCauses('hudson.model.Cause$UserIdCause')
                    echo "currentBuild value is ${currentBuild}"
                    echo "currentBuild.getBuildCauses is ${currentBuild.buildCauses}"
                    echo "userIdCause value is ${userIdCause}"
                    echo "userIdCause.size() value is ${userIdCause.size()}"
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
