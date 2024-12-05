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
                script {
                    String rootDir = pwd() + '/vars/'
                    Object testModule = load "${rootDir}@script/test1.groovy"
                    testModule.call()
                }
            }
        }
    }
}

