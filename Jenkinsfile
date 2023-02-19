pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh "g++ -o PES1UG20CS475-1 pes.cpp"
      }
    }
    stage('Test') {
      steps {
        sh "./PES1UG20CS475-1"
      }
    }
    
  }

  post {
    always {
      script {
        if (currentBuild.result != "SUCCESS") {
          echo "Pipeline failed"
        }
      }
    }
  }
}
