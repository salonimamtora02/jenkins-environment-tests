pipeline {
    agent any
     environment {
        Region1 = 'ca-central-1'
        Region2 = 'US-east-2'
        Test = 'Demo'
    }

    stages {
        stage('Hello') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'main') {
                        sh "echo 'Hello from main branch $Test'"
                    }  else {
                        sh "echo 'Hello Region is := $Region1'"
                    }
                    }
            }
        }
    }
}