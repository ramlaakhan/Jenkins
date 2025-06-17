parameters {
    booleanParam(name: 'executeTests', defaultValue: true, description: 'Run Tests')
}

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
                echo 'Testing Project'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project'
            }
        }
        stage('Conditional Test') {
            when {
                expression { return params.executeTests }
            }
            steps {
                echo 'Running conditional test stage...'
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
