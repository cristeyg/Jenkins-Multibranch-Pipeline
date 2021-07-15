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
                    Execute==True
                }
            steps {
                script{
                    echo 'Updating Second Stage'
                }
            }
        }
        stage('Third') {
            when {
                Execute==False
            }
            steps {
                echo 'Step Three'
            }
        }
    }
}
