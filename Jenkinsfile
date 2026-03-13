pipeline {
    agent any

    stages {
        stage('Q2') {
            steps {
                sh "sudo docker ps -aq | xargs -r sudo docker rm -f"
                sh "sudo docker run -itd -p 90:80 --name Q2 httpd"
                sh "sudo docker cp index.html Q2:/usr/local/apache2/htdocs/"
            }
        }
    }
}
