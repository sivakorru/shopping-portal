pipeline {
  agent any
  stages {
    stage('built') {
      steps {
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        sh 'npm run package '
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline for shopping-portal b4 completed...'
    }

  }
}