pipeline {

    agent {
//       node { label 'workstation'}
        label 'JAVA'
    }

    stages {

        stage('Master Node') {
            steps {
                sh 'echo Hello'
            }
        }

        stage('Agent Node') {
//             agent {
//                 label 'JAVA'
//             }
            steps {
                sh 'echo Hi'
            }
        }
    }
}