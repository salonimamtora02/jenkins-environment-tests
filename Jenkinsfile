pipeline {
    agent any
    environment {
        Region1 = 'ca-central-1'
        Region2 = 'us-east-2'
        
    }


    stages {
        stage('Stage-1') {
            steps {
                echo 'Hello World'
                echo "Hello !!!"
            }
        }
        stage('stage-2') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'main' && 'dev') {
                       sh "echo ("Region is =$Region1")"
                    } else {
                        sh "echo (Region is =$Region2)"
                    }
                }
            }
         }
    }
}
