
pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                bat 'docker build -t myweb .'
                bat 'docker rm -f myweb-container || exit /b 0'
                bat 'docker run -d --name myweb-container -p 8082:80 myweb'
            }
        }
    }
}
