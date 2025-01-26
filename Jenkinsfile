pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                script {
                    sh ' echo " starting to build" '
                    sh ' sudo docker build -t simple-flask-app:latest .'
                    sh '  docker run -d -p 5000:5000 simple-flask-app ' 
                    sh ' curl http:127.0.0.1:5000 '
                }
            }
        }

    stage('test') {
        steps {
            script {
                sh ' echo " test " '
                sh ' curl http:127.0.0.1:5000 '
            }
        }
    }

        stage('deploy') {
            steps {
                script {
                    sh 'echo "test" '
                }
            }
        }
        
    }
}
