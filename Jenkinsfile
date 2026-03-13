pipeline {
    agent any

    stages {
        stage('Q1') {
            steps {
                sh "sudo docker ps -aq | xargs -r sudo docker rm -f"
                sh "sudo docker run -itd -p 80:80 --name Q1 httpd"
                sh "sudo docker cp index.html Q1:/usr/local/apache2/htdocs/"
            }
        }
    }
}
