pipeline {
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
               bat ''' 
                ls 
                docker info 
                docker build -t reactFrontend . 
                docker images
                docker run --rm reactFrontend

                '''
            }
        }
    }
}