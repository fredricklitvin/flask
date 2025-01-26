pipeline {
    agent all
    stages {
        stage('build') {
            steps {
                script {
                    sh ' sudo python hello.py'
                  
                }
            }
        }

    stage('deploy') {
        steps {
            script {
                echo 'creating index.html'
                sh 'sudo cp /home/ec2-user/workspace/web-starter/index.html /var/www/html/index.html'
            }
        }
    }

        stage('check') {
            steps {
                script {
                    echo 'checking if it works'
                    sh 'sudo curl curl http://44.202.214.37:80'
                }
            }
        }
        
    }
}
