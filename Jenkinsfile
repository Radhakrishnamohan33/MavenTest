pipeline {
  agent any
  options {
    buildDiscarder logRotator(daysToKeepStr: '10', numToKeepStr: '9')
  }
  parameters {
    choice choices: ['develop', 'qa', 'master'], description: 'Choose the branch to build', name: 'branchName'
  }
  stages {
    stage('first stage') {
      steps {
        echo 'first stage'
      }
    }
  }
    
  post {
    success {
      echo 'stage success'
      cleanWs()
    }
  }
}
