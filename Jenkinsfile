pipeline {
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
               bat ''' 
                ls 
                docker info 
                docker build -t reactFrontend:${BUILD_NUMBER} . 
                docker tag reactFrontend:${BUILD_NUMBER} reactFrontend:latest 
                docker images
                '''
            }
        }
    }
}