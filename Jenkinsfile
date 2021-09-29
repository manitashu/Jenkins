pipeline {

    agent {
      node { label 'workstation'}
      label 'JAVA'
      none
    }

    agent any

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
                sh 'echo Hi'
            }
        }
    }

    post {

        always {
        //print 'Post Steps'
        sh 'echo Post Steps'
        }

    }
}

// pipeline {
//
//     agent any
//     options { disableConcurrentBuilds() }
//     tools {
//         maven 'maven'
//     }
//
//     parameters {
//             string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//             text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//             booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//             choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//             password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//         }
//
//     environment {
//         DEMO_URL = "google.com"
//         SSH = credentials('CENTOS_SSH')
//     }
//
//     stages {
//         stage('One') {
//
//             environment {
//                     DEMO_URL = "yahoo.com"
//                 }
//
//             steps {
//                 sh 'echo ${DEMO_URL}'
//                 echo "${SSH_USR}"
//             }
//
//         }
//
//         stage('Compile') {
//
//             input {
//                 message "Should we continue?"
//                 ok "Yes, we should."
// //                 submitter "alice,bob"
// //                 parameters {
// //                 string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//                 }
//
//             steps {
//                 sh 'ls'
//             }
//         }
//
//         stage('Three') {
//             parallel {
//                 stage('P1') {
//                     steps {
//                         sh 'sleep 30'
//                     }
//                 }
//
//                 stage('P2') {
//                     steps {
//                         sh 'sleep 30'
//                     }
//                 }
//
//                 stage('P3') {
//                     steps {
//                         sh 'sleep 30'
//                     }
//                 }
//             }
//         }
//     }
// }