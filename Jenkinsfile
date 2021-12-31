pipeline {
  agent any
  stages {
    stage('Verificar SCM') {
      steps {
        sh 'git rev-parse --short HEAD > .git/commit-id'
        sh 'gitcommit = readFile(\'.git/commit-id\').trim()'
        sh 'echo $gitcommit'
      }
    }

  }
  environment {
    gitcommit = '${gitcommit}'
  }
}