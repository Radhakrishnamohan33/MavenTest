@Library('sharedlib') _
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
        welcome ("RK")
        echo 'first stage'
        echo '$Names'
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
