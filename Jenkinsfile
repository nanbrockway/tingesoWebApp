pipeline {
  agent any
  
  stages {
    stage('Install') {
      steps { sh 'npm install' }
    }

    stage('Static code analysis') {
        steps { sh 'npm run-script lint' }
    }

    stage('Unit tests & build') {
        steps { sh 'npm run-script citest' }
    }

    stage('Build') {
      steps { sh 'npm run-script build' }
    }
    // stage('Test') {
    //   parallel {
    //     stage('Static code analysis') {
    //         steps { sh 'npm run-script lint' }
    //     }
    //     stage('Unit tests') {
    //         steps { sh 'npm run-script test' }
    //     }
    //   }
    // }

  }
}