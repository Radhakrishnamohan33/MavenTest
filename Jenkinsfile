@Library('sharedtest') _
pipeline {
  agent any
  options {
    buildDiscarder logRotator(daysToKeepStr: '10', numToKeepStr: '7')
  }
  parameters {
    choice choices: ['develop', 'qa', 'master'], description: 'Choose the branch to build', name: 'branchName'
  }
  stages {
    stage('first stage') {
      steps {
        welcome ("Prakashbabu")
        echo 'first stage'
      }
    }
  }
    
  post {
    success {
      echo 'stage success, thank you running the stage'
      cleanWs()
    }
  }
}
