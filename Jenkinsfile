pipeline {
    agent any

    stages {
        stage('Kubernetes Deploy') {
            //  environment {
            //     DISTRIBUTION = "E3I6JFKOQWMVWK"
            // }
            steps{
                script{
                     withEnv(readFile('env.' + env.BRANCH_NAME + '.txt').split('\n') as List) {
                        sh '''
                        echo ${REGION}
                        echo ${namespace}
                        echo ${cluster_name}
                        echo ${distibution_id}
                        '''

//                         sh 'aws eks --region ${REGION} update-kubeconfig --name ${cluster_name}'                   
//                         sh 'helm upgrade --install -n ${namespace} --create-namespace frontend frontend/ --set image.tag=$BUILD_NUMBER-$BRANCH_NAME'
//                         sh 'aws cloudfront create-invalidation --distribution-id ${DISTRIBUTION} --paths "/*"'
                     }  
                }                 
            }
        }
    }
}
