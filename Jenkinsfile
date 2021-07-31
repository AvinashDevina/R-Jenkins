//pipeline {
//
////  agent {
////    //node { label 'workstation' }
////    //label 'JAVA'
////    any
////  }
//
//  agent  any
//
//  stages {
//
//    stage('Master Node') {
//      agent {
//        label 'MASTER'
//      }
//      steps {
//        sh 'echo Hello'
//      }
//    }
//
//    stage('Agent Node') {
//      agent {
//        label 'JAVA'
//      }
//      steps {
//        sh 'echo Hello'
//      }
//    }
//
//  }
//
//  post {
//
//    always {
//      sh 'echo Post Steps'
//    }
//
//  }
//
//}

pipeline {
  agent any
  options { disableConcurrentBuilds() }

  environment {
    DEMO_URL = "google.com"
    SSH = credentials('CENTOS_SSH')
  }

  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
  }

  stages {
    stage('One') {
      environment {
        DEMO_URL = "yahoo.com"
      }
      steps {
        sh 'echo ${DEMO_URL}'
        echo "${SSH_USR}"
        echo "PERSON = ${PERSON}"
      }
    }
  }
}