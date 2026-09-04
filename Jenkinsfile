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
                    sh printenv
            }
    }

}