pipeline {
  agent any

  stages {

    stage('Prepare Artifacts') {
      steps {
        sh '''
          zip ../todo.zip *
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