pipeline {
  agent {
    node {
      label 'master'
      customWorkspace 'pipelineWorkspace'
    }

  }
  stages {
    stage('begin') {
      parallel {
        stage('begin') {
          steps {
            echo 'hello pipeline begin'
          }
        }

        stage('Parallel Steps') {
          steps {
            sh 'echo "Begin Step"'
          }
        }

      }
    }

    stage('running') {
      parallel {
        stage('running') {
          steps {
            echo 'hello pipeline running'
          }
        }

        stage('running 2') {
          steps {
            sh 'echo "This is running 2"'
          }
        }

      }
    }

    stage('finish') {
      steps {
        echo 'hello pipeline finish'
        sh 'exit 0'
      }
    }

  }
  post {
    success {
      echo 'goodbye pipeline success!'
    }

    failure {
      echo 'ops!!! pipeline failed....'
    }

    always {
      echo 'always say goodbye'
    }

  }
}