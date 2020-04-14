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
        sh 'git version'
        sh 'java -version'
        sh 'docker version'
      }
    }
    stage('deploy to QA') {
      when {
         branch 'develop'
      }
      steps {
        echo 'deploy to QA to test'
      }
    }
    
    stage('deploy to UAT') {
      when {
         branch 'release'
      }
      steps {
        echo 'deploy to UAT'
      }
    }
    
    stage('deploy to production') {
      when {
         branch 'master'
      }
      steps {
         echo 'deploy to production'
      }
    }
  }
}
