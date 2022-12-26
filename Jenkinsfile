pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                sh 'cd SimpleSpringBoot'
                sh 'printenv'
            }
        }
        stage("Setup Env"){
            steps{
                sh "sudo apt-update"
            }
        }
        stage("Deploy"){
            steps{
                sh "cd SimpleSpringBoot && cp build/* /files"
            }
        }
        
    }
   // post{
        // success{
        //     archiveArtifacts artifacts: '**/build', followSymlinks: false
        // }
        // failure{
        //     emailext body: '''Jenkins has failed to build the Job. Please find the information below.

        //                     Name of the Job: ${JOB_NAME}
        //                     Build that failed: ${BUILD_NUMBER}

        //                     Please check the logs at ${BUILD_URL}


        //                     Thanks
        //                     Jenkins''', subject: 'Failed ${JOB_NAME}', to: 'basil@coit.io'
        // }
   // }
}
