pipeline {
    agent any

    stages {
        stage('First') {
            steps {
                script{
                    env.EXECUTE="True"
                }
            }
        }
        stage('Second') {
            when {
                ${EXECUTE}=="True"
                }
            steps {
                script{
                    echo 'Updating Second Stage'
                }
            }
        }
        stage('Third') {
            when {
                ${EXECUTE}=="False"
            }
            steps {
                echo 'Step Three'
            }
        }
    }
}
