pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    withEnv(readFile('env.' + env.BRANCH_NAME + '.txt').split('\n') as List) {
                        sh "echo ${REGION}"
                    }

                 }
            }
        }
    }
}