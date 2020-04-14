pipeline {
  agent any
  stages {
    stage('source') {
      steps {
        echo env.BRANCH_NAME
        echo 'hello world'
      }
    }
    stage('execute sh commands') {
      steps {
        sh 'ls -la'
        sh 'mvn -v'
        sh 'sudo docker version'
      }
    }
  }
}
