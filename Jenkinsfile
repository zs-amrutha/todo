@Library('todoapp') _

pipeline {
  agent {
    label 'NODEJS'
  }

  stages {

    stage('Download Dependencies') {
      steps {
        sh '''
          npm install
        '''
      }
    }

    stage('Prepare Artifacts') {
      steps {
        sh '''
          zip -r todo.zip node_modules server.js
        '''
      }
    }

    stage('Upload Artifact') {
      steps {
        script {
          nexus
        }

      }
    }
  }

}