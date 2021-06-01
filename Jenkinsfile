pipeline {
  agent any

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
        sh '''
         curl -v -u admin:admin123 --upload-file /home/ubuntu/workspace/TODO_CI-Pipelines/todo.zip http://172.31.52.12:8081/repository/todo/todo.zip
        '''
      }
    }
  }

}