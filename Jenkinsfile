pipeline {

  agent {
    //node { label 'workstation' }
    //label 'JAVA'
    any
  }

  stages {

    stage('Master Node') {
      agent {
        label 'MASTER'
      }
      steps {
        sh 'echo Hello'
      }
    }

    stage('Agent Node') {
      agent {
        label 'JAVA'
      }
      steps {
        sh 'echo Hello'
      }
    }

  }
}
