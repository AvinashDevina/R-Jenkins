pipeline {

//  agent {
//    //node { label 'workstation' }
//    //label 'JAVA'
//    any
//  }

  agent  none

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

  post {

    agent any
    
    always {
      sh 'echo Post Steps'
    }

  }

}
