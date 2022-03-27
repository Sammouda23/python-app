pipeline {
  agent any
  stages {
    stage("build") {
      steps {
        sh """
          docker build -t hello_there .
        """
      }
    }
    stage("run") {
      steps {
        sh """
          docker run -d  hello_there
  
        """
      }
    }
    stage("Testing") {
      steps {
        sh """
          docker run -d  hello_there
  
        """
      }
    }
  }
}
