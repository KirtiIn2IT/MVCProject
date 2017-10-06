pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'echo Build'
      }
    }
    stage('Backend') {
      steps {
        parallel(
          "Unit": {
            bat 'echo Unit'
            
          },
          "Performance": {
            bat 'echo Performance'
            
          }
        )
      }
    }
    stage('Frontend') {
      steps {
        parallel(
          "Frontend": {
            bat 'echo Frontend'
            
          },
          "More Test": {
            bat 'echo More Test'
            
          }
        )
      }
    }
    stage('Static Analysis') {
      steps {
        bat 'echo StaticAnalysis'
      }
    }
    stage('Deploy') {
      steps {
        bat 'echo Deploy'
      }
    }
  }
}