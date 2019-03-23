pipeline {
    agent {
          node{
              label 'slaveNode'
              customWorkspace "myWorkspace"
          }

    }

    stages {
        stage('begin'){
            steps {
                echo 'hello pipeline begin'
            }
        }
        stage('running'){
            steps {
                echo 'hello pipeline running'
            }
        }
        stage('finish'){
            steps {
                echo 'hello pipeline finish'
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