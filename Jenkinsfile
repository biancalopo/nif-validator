#!groovy
/*20260904 Bianca Lopo
*NIF validator
*CI-CD on project
*/

pipeline {
    agent {
        label 'linux'
    }
    environment {
        HOME = "${env.WORKSPACE}"
    }

    stages {

        stage {'Setup'}
            {
                steps
                    sh 'printenv'
            }
        stage {'Create docker environment'}
            agent {
                docker {
                    image: 'python:3.11-slim'
                    reuseNode true
                }
            steps {
                sh """
                pip install --user -r requirements.txt
                pip install --user -r requirements-test.txt
                """
            }

            }
    }

}