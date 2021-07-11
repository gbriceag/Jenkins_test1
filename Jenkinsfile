pipeline {
  agent {
      label 'windows'
      
  }
  stages {
    stage('Stage 1') {
      steps {
        echo 'Hello wwwwwwworld!'
      }
    }
    stage('Stage 2') {
      steps {
        echo 'Hello George!'
      }
    }
    stage('Stage 3') {
      steps {
        bat 'python C:/Jenkins/scratch_1.py'
      }
    }
  }
  post {
    always {
      echo 'always runs regardless of the completion status of the Pipeline run'
    }
    success {
      echo 'step will run only if the build is successful'
    }
    failure {
      echo 'only when the Pipeline is currently in a "failed" state run, usually expressed in the Web UI with the red indicator.'
    }
    unstable {
      echo 'current Pipeline has "unstable" state, usually by a failed test, code violations and other causes, in order to run. Usually represented in a web UI with a yellow indication.'
    }
    changed {
      echo 'can only be run if the current Pipeline is running at a different state than the previously completed Pipeline'
    }
  }
}
