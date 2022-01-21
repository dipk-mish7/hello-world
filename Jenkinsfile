pipeline {
  agent any
  stages {
    stage('code checkout') {
      steps {
        sh 'echo "Git clone"'
      }
    }

    stage('init') {
      steps {
        sh '''echo "terraform init"
'''
      }
    }

    stage('validate') {
      steps {
        sh 'echo "validate"'
      }
    }

    stage('formatting') {
      steps {
        sh 'echo "formatting"'
      }
    }

    stage('lint') {
      steps {
        sh 'echo "lint"'
      }
    }

    stage('security') {
      steps {
        sh 'echo "security"'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "test"'
          }
        }

        stage('compliance') {
          steps {
            sh 'echo "terraform"'
          }
        }

      }
    }

    stage('apply') {
      steps {
        sh 'echo "apply"'
      }
    }

  }
}