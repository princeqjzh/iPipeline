pipeline {
    agent  any

    stages {
        stage('begin'){
            steps {
                echo 'hello pipeline begin'
            }
        }
    }

    post {
        success {
            echo 'goodbay pipeline success!'
        }

        failure {
            echo 'ops!!! pipeline failed....'
        }

        always {
            echo 'always say goodbay'
        }
    }
}