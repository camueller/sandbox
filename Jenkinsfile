pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                scmSkip(deleteBuild: false, skipPattern:'.*\\[ci skip\\].*')
            }
        }
        stage('Build') {
            steps {
                sh "mvn package"
            }
        }
    }
}
