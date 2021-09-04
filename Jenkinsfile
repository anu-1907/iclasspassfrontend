pipeline {
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
               bat ''' 
                ls 
                docker info 
                docker build -t reactFrontend . 
                docker tag reactFrontend reactFrontend:latest 
                docker images
                docker run --rm reactFrontend

                '''
            }
        }
    }
}