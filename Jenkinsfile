pipeline {
    agent any

    stages {
        stage('Q3') {
            steps {
                sh "sudo docker ps -aq | xargs -r sudo docker rm -f"
                sh "sudo docker run -itd -p 880:80 --name Q3 httpd"
                sh "sudo docker cp index.html Q3:/usr/local/apache2/htdocs/"
            }
        }
    }
}
