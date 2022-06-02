// declarative

pipeline {
    agent {
        label 'slave'
    }

    stages {
//         stage('Install black'){
//             steps{
//                 sh 'pip3 install black'
//             }
//         }

//         stage('Run black'){
//             steps{
//                 sh 'black .'
//             }
//         }
        
//         stage('Env Variables'){
//             steps{
//                 sh "printenv"
//                 script {
//                     if (env.BRANCH_NAME == null) {
//                         env.BRANCH_NAME = "N.A."
//                     }
//                     if (env.TAG_NAME == null) {
//                         env.TAG_NAME = "ANOTHER DIFFERENT THING"
//                     }
//                     if (env.EXTRA_GUARANTEED_NOT_TO_EXIST == null) {
//                         env.EXTRA_GUARANTEED_NOT_TO_EXIST = "1111pajfpjsapjzvl"
//                     }
//                     if (env.GIT_COMMIT == null) {
//                         env.GIT_COMMIT = "Whoopdeod"
//                     }
//                 }
//                 echo "BRANCH_NAME = ${env.BRANCH_NAME}"
                
//                 echo "TAG_NAME = ${env.TAG_NAME}"
                
//                 echo "guarantor = ${env.EXTRA_GUARANTEED_NOT_TO_EXIST}"
                
//                 //sh 'export BRANCH=${BRANCH_NAME:-\"N.A.\"}'
//                 //sh 'echo "$env.BRANCH"'
//                 echo "This is the git commit ${env.GIT_COMMIT}"
//             }
//         }
        
        stage('Run TestSigma Sanity on Production Test Plan') {
            steps{
                sh 'curl -X POST -H "Content-type: application/json" -H "Accept:application/json" -H "Authorization: Bearer eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiIwZTVmNzI3Ny01MDgzLTQ1OTYtYThlZi02ZGQ1MmViMTVjYmUiLCJkb21haW4iOiJzY2FudGlzdC5jb20iLCJ0ZW5hbnRJZCI6MzI0NDl9.i2pO5Z1vxCPPV209NShQYKYmhSjpGeBTWYLWrBmpEyJ-yZV32EknYFKQGescIiCF4CWgvzxjrCa69xF-5a3ujA" https://app.testsigma.com/api/v1/execution_results -d "{\"executionId\": \"506\"}"'
            }
        }
    }
}
