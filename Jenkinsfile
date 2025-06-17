flag-true

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
            }
        }
        stage('Test') {
            steps {
                when {
                    expression {
                        flag -- false
                    }
                }
                echo 'Testing Project'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project'
            }
        }
    }
    post {
    always {
        echo 'Post Build Condition Running'
    }
    failure {
        echo 'Post Action if Build Failed'
    }
}
}
