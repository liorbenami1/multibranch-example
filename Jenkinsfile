pipeline {
    agent none
    stages {
        stage('Example Build') {
            agent { docker 'levep79/jdk-alpine:latest' }
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            agent {
                docker 'maven:3.5-alpine'
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