pipeline {

//     agent {
//         node { label 'workstation'}
//         label 'JAVA'
//         any
//     }

    agent none

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
}