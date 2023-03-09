pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }

    stage('package') {
      parallel {
        stage('package') {
          steps {
            echo 'next build'
          }
        }

        stage('echo') {
          steps {
            sh 'echo "python -m flask run"'
          }
        }

      }
    }

  }
  environment {
    PYTHON_ENV = 'development'
  }
}