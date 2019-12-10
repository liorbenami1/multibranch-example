pipeline {
    agent {
        docker 'registry.hub.docker.com/levep79/jdk-alpine'
    }
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            agent {
                docker 'registry.hub.docker.com/maven:3-alpine'
            }
            when {
                beforeAgent true
                branch 'master'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}