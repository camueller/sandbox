pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                scmSkip(deleteBuild: true, skipPattern:'.*\\[ci skip\\].*')
            }
        }
        stage('Build') {
            steps {
                sh "mvn package"
            }
        }
    }
}
