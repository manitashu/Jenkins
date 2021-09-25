pipeline {

    agent {
        //node { label 'workstation'}
        //label 'JAVA'
        none
    }

    stages {

        stage('Master Node') {
            agent {

            }
            steps {
                sh 'echo Hello'
            }
        }

        stage('Agent Node') {
            steps {
                sh 'echo Hi'
            }
        }
    }
}