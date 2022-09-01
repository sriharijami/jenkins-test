peline {
  agent {
    node {
      label 'nodejs'
    }
  }
  stages {
    stage ('Creating a new application') {
      steps {
        sh 'oc new-app --name jenkins quay.io/sriharijami/srihari-static-web'
      }
    }
  }
  post {
    failure {
      echo 'FAILED'
      sh 'oc status'
    }
    success {
      sh 'oc status'
      sh 'oc get all'
      sh 'oc get pods'
      echo 'SUCCESS'
    }
  }
}
