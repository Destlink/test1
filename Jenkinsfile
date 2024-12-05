void test1() {
    sh script:'echo groovy'
}

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('merge') {
            when {
                branch "develop"
            }
            steps {
                sh '''
                    echo 'on develop'
                '''
                test1()
            }
        }
    }
}

