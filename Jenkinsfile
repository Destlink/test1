pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('merge') {
            with {
                branch: 'develop'
            }
            steps {
                sh '''
                    echo 'on develop'
                '''
            }
        }
    }
}

